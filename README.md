# Ticket Allocator and Ticket Bundle Splitter

A web application for organising theatre seating allocations and turning a combined ticket PDF into booking-specific ticket bundles.

## Project overview

The project supports two related tasks: assigning groups to suitable available seats, and matching allocated seats to ticket pages so each booking receives the appropriate documents.

## Key capabilities

- Import booking and seat information from structured files.
- Expand seat ranges into individual seat records.
- Allocate contiguous seats while considering group size, accessibility, section and seating preferences.
- Flag unmatched bookings and cases requiring manual review.
- Match ticket pages to bookings and preview the results.
- Generate per-booking PDFs, ZIP bundles and an allocation manifest.
- Generate Apple Wallet pass files, with signing support when certificates are configured.
- Support large-PDF upload workflows through Vercel Blob.

## Tech stack

| Area | Technologies |
| --- | --- |
| Backend | Python, FastAPI, Uvicorn, Pydantic |
| Frontend | JavaScript, HTML, CSS |
| PDF processing | pypdf, PyMuPDF |
| Image and barcode processing | OpenCV, zxing-cpp |
| Wallet signing | cryptography |
| Spreadsheet support | CSV processing, numbers-parser |
| Hosting integration | Vercel Functions, Vercel Blob, Node.js upload handlers |
| Tests | Python automated tests |

## Engineering focus

Deterministic seat identities, preference-based allocation, preserving booking-to-ticket correspondence, handling varied input formats and surfacing ambiguous matches for review.

## Status and scope

Application implementation with API documentation and automated test coverage. Wallet installation depends on valid signing configuration, and unstructured seat-plan imports require manual confirmation. This overview does not claim a currently active deployment.

## About this repository

This public repository contains only a project overview. Source code, operational configuration, ticket files, booking data and original commit history remain private.
