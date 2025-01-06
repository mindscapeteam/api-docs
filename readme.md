# Mindscape Health API

Welcome to the **Mindscape Health API**! This API allows developers to integrate with our platform to fetch therapist details and verify therapist credentials.

## Base URL  
```
https://api.mindscapehealth.org
```

## Endpoints  

### 1. **Get a List of Therapists**  
Retrieve a list of therapists registered on the platform.  

- **Endpoint**:  
  ```
  GET /dev/therapists
  ```
- **Headers**:  
  ```
  Authorization: Bearer <your-auth-key>
  ```
- **Response**:  
  ```json
  [
      {
          "display_name": "Leon Kipkoech",
          "location": "Nairobi",
          "specializationAreas": ["Trauma and PTSD", "Relationship Issues"],
          "preferredLanguages": ["English", "Swahili"],
          "therapeuticApproaches": ["CBT", "Solution-Focused Therapy"]
      }
  ]
  ```

### 2. **Verify Therapist Credentials**  
Verify the details of a specific therapist. The therapist must be registered on the platform.  

- **Endpoint**:  
  ```
  POST /dev/therapist
  ```
- **Headers**:  
  ```
  Authorization: Bearer <your-auth-key>
  ```
- **Request Body**:  
  ```json
  {
      "therapist_name": "12345",
      "therapist_dob": "01/01/2001",
  }
  ```
- **Response**:  
  ```json
  {
      "therpist_name": "Leon Kipkoech",
      "location": "Nairobi",
      "pronouns": "he/him/his",
      "offering": ["In-person sessions", "Insurance options"],
      "specializationAreas": ["Trauma and PTSD", "Relationship Issues"],
      "therapeuticApproaches": ["CBT", "Solution-Focused Therapy"],
      "selected_topics": ["Stress Management", "Addiction and Substance Abuse"],
      "preferredLanguages": ["English", "Swahili"],
      "years_of_experience": 2,
      "charges_per_session": 2000
  }
  ```

## Authentication  

All requests require an **Authorization Key** in the headers.  
Developers can request an API key by emailing **[hello@mindscapehealth.org](mailto:hello@mindscapehealth.org)**.

Example Header:  
```http
Authorization: Bearer <your-auth-key>
```

## Contact  

For questions or support, please reach out to us at **[hello@mindscapehealth.org](mailto:hello@mindscapehealth.org)**.  
