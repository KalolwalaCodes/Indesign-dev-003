# PDF Comment and Feedback System

A collaborative platform that enables clients to mark up and comment on PDF documents, with designers able to review, respond, and mark comments as resolved directly in InDesign.

## Overview

This application bridges the gap between client feedback and designer implementation by providing a streamlined workflow for document review and revision. Clients can select portions of PDF documents to add comments, while designers can view, respond to, and track the status of these comments within their InDesign workflow.

## Tech Stack

### Backend
- **NestJS**: A progressive Node.js framework for building efficient and scalable server-side applications
- **TypeORM**: Object-relational mapping for database interactions
- **PostgreSQL**: Primary database for storing user data, comments, and document metadata
- **JWT**: Authentication and secure API access
- **Socket.IO**: Real-time notifications and live updates

### Frontend
- **Next.js**: React framework for server-rendered applications
- **React PDF**: For PDF rendering and interaction
- **TailwindCSS**: Utility-first CSS framework for styling
- **Redux Toolkit**: State management
- **Axios**: HTTP client for API calls

### Integration
- **InDesign Plugin**: Custom InDesign extension that connects to our platform API
- **AWS S3**: Document storage and retrieval
- **SendGrid**: Email notifications

## Key Features

### For Clients
- PDF document upload and viewing
- Text selection and highlighting in PDFs
- Comment creation with priority levels
- Real-time collaboration
- Comment history and version tracking

### For Designers
- InDesign integration to view comments in context
- Comment status management (pending, in-progress, resolved)
- Reply functionality to client comments
- Batch operations for similar comments
- Export revision history

## Architecture

The application follows a microservices architecture:

1. **Authentication Service**: Handles user registration, login, and permissions
2. **Document Service**: Manages PDF uploads, storage, and retrieval
3. **Comment Service**: Processes comment creation, updating, and querying
4. **Notification Service**: Handles real-time updates and email notifications
5. **InDesign Plugin Service**: Facilitates communication between the web platform and InDesign

## Getting Started

### Prerequisites
- Node.js (v14+)
- PostgreSQL
- Adobe InDesign (for designer features)
- AWS account (for S3 storage)

### Installation

1. Clone the repository
```bash
git clone https://github.com/your-organization/pdf-comment-system.git
cd pdf-comment-system