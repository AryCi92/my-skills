---
name: angular-api-service-standard
description: Generate Angular API services following company standards using HttpClient, typing, and best practices
tags: [angular, api, service, standards]
---

# Angular API Service Standard

## Overview
Questa skill genera servizi API Angular seguendo gli standard aziendali, includendo tipizzazione forte, gestione errori e struttura modulare.

## How this skill works
La skill prende in input una descrizione delle API e genera un service Angular che:
- usa HttpClient
- è completamente tipizzato
- segue naming convention aziendale
- centralizza la gestione degli errori
- è compatibile con standalone architecture

## When to use it
Usa questa skill quando:
- devi creare un nuovo service API
- vuoi uniformare servizi esistenti
- stai integrando nuove API backend

## Best practices
- Usa sempre tipi espliciti (no `any`)
- Separa modelli (DTO) dal service
- Centralizza base URL e headers
- Gestisci errori con RxJS (`catchError`)
- Mantieni metodi piccoli e specifici

## Input
Descrivi:
- nome della risorsa (es. users, orders)
- endpoint disponibili
- struttura dati

## Instructions
Generate an Angular service based on the following input:

{{input}}

Requirements:
- Use Angular HttpClient
- Use standalone injectable service
- Use RxJS best practices
- Include CRUD methods if applicable (getAll, getById, create, update, delete)
- Use strong typing with interfaces
- Add error handling with catchError
- Follow clean and readable structure

## Output
Return only valid TypeScript code for the Angular service.

## Example

### Input
Create a service for managing users with:
- GET /users
- GET /users/:id
- POST /users
- PUT /users/:id
- DELETE /users/:id

### Output
```ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable, catchError, throwError } from 'rxjs';

export interface User {
  id: number;
  name: string;
  email: string;
}

@Injectable({
  providedIn: 'root'
})
export class UserService {
  private baseUrl = '/api/users';

  constructor(private http: HttpClient) {}

  getAll(): Observable<User[]> {
    return this.http.get<User[]>(this.baseUrl)
      .pipe(catchError(this.handleError));
  }

  getById(id: number): Observable<User> {
    return this.http.get<User>(`${this.baseUrl}/${id}`)
      .pipe(catchError(this.handleError));
  }

  create(user: User): Observable<User> {
    return this.http.post<User>(this.baseUrl, user)
      .pipe(catchError(this.handleError));
  }

  update(id: number, user: User): Observable<User> {
    return this.http.put<User>(`${this.baseUrl}/${id}`, user)
      .pipe(catchError(this.handleError));
  }

  delete(id: number): Observable<void> {
    return this.http.delete<void>(`${this.baseUrl}/${id}`)
      .pipe(catchError(this.handleError));
  }

  private handleError(error: any) {
    console.error('API error:', error);
    return throwError(() => error);
  }
}