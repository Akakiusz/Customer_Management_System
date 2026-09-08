# NOUVEM — Customer Management System

A small customer management app. It does the four basic
things you'd expect from a customer list: add, view, edit, and delete
customers (the classic CRUD operations).

The whole thing is a single `index.html` file — HTML, CSS and a bit of
JavaScript, no libraries and no build step. Just open it in a browser and
it works.

## Try it

Open `index.html` in any browser. That's it. Nothing to install.

## What it does

- **Add** a customer through the form at the top
- **See** all customers in a table
- **Edit** anyone — their details load back into the form
- **Delete** a customer (it asks first, so you don't nuke someone by accident)
- Each customer has a name, company, email, phone, and an Active/Inactive status

## A few notes on how I built it

- **The data lives in a plain JavaScript array.** This is a mock-up, so there's
  no real database — the array is the "database". I kept everything routed
  through one `render()` function that redraws the table from that array, so
  the screen and the data can never drift out of sync.

- **One form does both Add and Edit.** A hidden field remembers whether you're
  creating someone new or updating an existing record. Felt cleaner than
  building two near-identical forms.

- **The colours follow NOUVEM's own branding** — the steel blue and orange from
  the logo, on a light grey background. The slogan is NOUVEM's actual tagline.

## What I'd do next in a real version

This is deliberately kept simple for the task. If it were going to production
I'd:

- Swap the array for a real backend/API — and because everything already goes
  through that one array, that's pretty much the only part that would change
- Save the data properly (a database, or at least the browser's local storage
  so it survives a refresh)
- Escape user input before showing it, to be safe against dodgy input
- Add search, sorting, and validation on the email field

## Files

- `index.html` — the whole app, in one file