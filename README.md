# VectorShift Frontend Technical Assessment

This repository contains my submission for the **VectorShift (YC S23) Frontend Technical Assessment**.  
The project demonstrates scalable frontend architecture, dynamic node behavior, clean UI styling, and backend integration using FastAPI.

---

## 🧠 Overview

The application is a **node-based pipeline editor** that allows users to create pipelines using different node types, connect them with edges, and submit the pipeline to a backend service for validation.

The implementation focuses on:
- Reusable and extensible node abstractions
- Clean and unified UI design
- Dynamic text node behavior
- Full-stack integration with DAG validation

---

## 🛠 Tech Stack

### Frontend
- **React**
- **JavaScript**
- **React Flow**
- CSS / Tailwind (for styling)

### Backend
- **Python**
- **FastAPI**
- **Uvicorn**

---

## ✨ Features Implemented

### 1. Node Abstraction
- Created a reusable `BaseNode` component to eliminate duplication across node types
- Existing nodes (Input, Output, LLM, Text) were refactored to use this abstraction
- Added 5 new nodes to demonstrate scalability and flexibility

### 2. Styling
- Applied a clean, unified design across all nodes
- Consistent spacing, typography, and layout
- Focused on clarity and usability over heavy animations

### 3. Text Node Enhancements
- Auto-resizing text input based on content
- Dynamic variable detection using `{{ variable }}` syntax
- Automatically generates input handles for detected variables
- Handles update dynamically as text changes

### 4. Backend Integration
- Frontend submits pipeline nodes and edges to the backend
- Backend calculates:
  - Number of nodes
  - Number of edges
  - Whether the pipeline is a Directed Acyclic Graph (DAG)
- Results are displayed to the user in a clear, user-friendly alert

---

## 🚀 Running the Project Locally

### Prerequisites
- Node.js (v16+ recommended)
- Python 3.9+

---

### Frontend Setup
```bash
cd frontend
npm install
npm start
