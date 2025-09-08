Class 04

# Automation with n8n, Airtable & Discord

This README provides a concise guide to building and running workflows using **n8n**, Airtable, and Discord.

---

## Credentials & Setup

- Sign up and generate **API credentials** (API key, username, password).
- Create a **Personal Access Token** from _Builder Hub → Developers → Tokens_.
- Select proper **Scopes**: Schema Read, Records Read, Records Write.
- Assign token to the correct **Base** (e.g., _Nathan Orders Book_).

---

## 🛠 Applications Needed

- **Data Warehouse API** → Source of company data.
- **Airtable** → Table management and record storage.
- **Discord** → Notifications via Webhooks.

---

## Workflow Setup in n8n

### 1. Create Workflow

- New workflow → Name (e.g., _Mini Workflow_), add a tag (e.g., _Penaverse_).
- Add nodes as required.

### 2. Adding Nodes

- Methods:
  1. Plus (+) button → Add next node.
  2. Press **Tab** → Open node panel.
  3. Drag node from panel to canvas.
- Connect nodes by dragging from one node’s output to another node’s input.

### 3. Node Configuration

- **Required Parameters** → Must be filled.
- **Optional Parameters** → Found under _Additional Fields_.
- Node Colors:
  - ✅ Green → Ready
  - ⚠️ Yellow → Config ok but no input
  - ❌ Red → Missing required parameters

---

## 📊 Airtable Table Schema

Create a table with the following columns:

1. Order ID → Number
2. Customer ID → Number
3. Employee Name → Text
4. Order Price → Decimal/Float
5. Status → Text

---

## 🔄 Workflow Steps

1. **Connect Airtable**

   - Create credentials → Paste token.
   - Select Base + Table.
   - Enable **Auto Mapping**.
   - Execute → Data syncs to Airtable.

2. **Filter Data**

   - Add **IF Node** to filter by Status:
     - True → Processing Orders.
     - False → Booked Orders.

3. **Custom Mapping**

   - Create a “Sales Team” table with only `Order ID` + `Employee Name`.
   - Map and execute → Only those columns saved.

4. **Duplicate Views**

   - Example: Duplicate “All Orders” → Rename (e.g., _Processing Orders_, _Sales Team_).

5. **Perform Calculations**

   - Add **Code Node (JavaScript)**:
     - Count total records.
     - Sum of Order Price.
   - Output: `Book Count`, `Book Sum`.

6. **Send Results to Discord**
   - Add **Discord Node → Send Message**.
   - Connect via Webhook URL.
   - Map calculated results.
   - Execute → Message sent to channel.

---

## 🚨 Common Issues

- **Workflow Activation** → Needs a trigger node (e.g., webhook).
- **Execution Errors** → Usually caused by wrong credentials or missing parameters.
- **Email Delay** → Sometimes emails may not be delivered instantly (retry later).

---

## 🔄 Alternatives

- **Google Sheets** can be used instead of Airtable.
- **Webhook vs API**:
  - API = Request/response.
  - Webhook = Automatic push from system.

---

✅ Using this workflow, repetitive tasks like **data fetch, filtering, calculation, and reporting** can be fully automated.
