# Technical Documentation

#### `/report/cogs-report` - `GET`

```mermaid
   graph TD
      A[Start: COGS Report Generation]
      B[Initialization: Instantiate PrimeCostReportController]
      C[Adjust Categories: Check and unset 'categories' if 'all']
      D[Adjust Comps Accounts: Check and unset 'comps_accounts' if 'all']
      E[Fetch Prime Cost Data]
      F[Check Authentication: Is user authenticated?]
      G[Yes: Construct API Response]
      H[No: Render Web View]
      I[Process Date Ranges: Weekly, Monthly, Yearly, etc.]
      J[Generate COGS Data: Based on date range]
      K[Generate Prime Cost Data: Based on date range]
      L[Fetch Chart Data: Prime Cost & Profit]
      M[End]

      A --> B
      B --> C
      C --> D
      D --> E
      E --> I
      I --> J
      J --> F
      I --> K
      K --> F
      F --> G
      F --> H
      E --> L
      L --> M
```

#### `/report/cogs-report/detailed/run` - `POST`

```mermaid
   graph TD
      A[Start: Detailed COGS Report Generation]
      B[Set: Initialize comps_accounts from request]
      C[Adjust Categories: Check and unset 'categories' if 'all']
      D[Adjust Comps Accounts: Check and unset 'comps_accounts' if 'all']
      E[Initialization: Instantiate PrimeCostReportController]
      F[Set: Mark request for COGS report]
      G[Check: API Authentication]
      H[Is API Authenticated?]
      I[Yes: Process Request for API]
      J[No: Return View for Web]
      K[Set Sales Data]
      L[Set Purchases Data]
      M[Calculate COGS: Cost of Goods Sold]
      N[Calculate Total COGS]
      O[Process Date Ranges]
      P[Set Report Date & Run-On Date]
      Q[Check: API Authentication Again]
      R[Yes: Process Discounts & Return API Response]
      S[No: Check if Export Requested]
      T[Yes: Export Data]
      U[No: Render Web View]
      V[End]

      A --> B
      B --> C
      C --> D
      D --> E
      E --> F
      F --> G
      G --> H
      H --> I
      H --> J
      I --> K
      K --> L
      L --> M
      M --> N
      N --> O
      O --> P
      P --> Q
      Q --> R
      Q --> S
      S --> T
      S --> U
      T --> V
      U --> V
```

#### `/report/compare-report` - `POST`

```mermaid
   graph TD
      A[Start: Compare Reports Generation]
      B[Validation: Ensure 'params' exist in request]
      C[Initialization: Decode request parameters]
      D[Loop: For each 'items' in params]
      E[Create new Request instance]
      F[Assign parameters to the new request]
      G[Fetch daily sales for the given parameters]
      H[Prepare data for the comparison]
      I[End of loop]
      J[Check: API Authentication]
      K[Yes: Format & Return API Response]
      L[No: Return totals]
      M[End]

      A --> B
      B --> C
      C --> D
      D --> E
      E --> F
      F --> G
      G --> H
      H --> I
      I --> J
      J --> K
      J --> L
      K --> M
      L --> M
```

#### `/report/detailed/cogs-report` - `GET`

```mermaid
   graph TD
      A[Start: Detailed COGS Report Generation]
      B[Check: Categories & Comps Accounts]
      C[Initialize: PrimeCostReportController]
      D[Set: cogs_report in request to true]
      E[Check: API Authentication & api_cogs_inventory]
      F[Yes: Modify request for categories & comps accounts]
      G[Fetch: Detailed Prime Cost Report]
      H[No: Fetch & GetData from Detailed Prime Cost Report]
      I[Modify & Set: Sales, Purchases, COGS and Total COGS]
      J[Extract: All request data]
      K[Check: Date Range]
      L[Yes: Convert & Format Dates]
      M[No: Set dates to null]
      N[Get: Current Date & Format]
      O[Check: API Authentication]
      P[Yes: Handle Discounts & Prepare Data]
      Q[Return: API Response]
      R[No: Check if export]
      S[Yes: Return exported data]
      T[No: Return view with data]
      U[End]

      A --> B
      B --> C
      C --> D
      D --> E
      E --> F
      F --> G
      E --> H
      G --> I
      H --> I
      I --> J
      J --> K
      K --> L
      K --> M
      L --> N
      M --> N
      N --> O
      O --> P
      P --> Q
      O --> R
      R --> S
      R --> T
      Q --> U
      S --> U
      T --> U

```

#### `/report/detailed/prime-cost-report` - `POST`

```mermaid
   graph TD
      A[Start: Detailed Prime Cost Report Generation]
      B[Initialize: Date, Restaurant, CogsReportController]
      C[Check: Date Range]
      D[Set: From & To Dates from Request]
      E[Fetch: Sales based on Date Range]
      F[Modify: Request with Date Range]
      G[Check: Report Version]
      H[Yes: Modify Sales using setSales]
      I[No: Modify Sales using setSales2]
      J[Calculate: Total Sales]
      K[Check: Restaurant Comps & Request Comps]
      L[Yes: Handle Comps Adjustments]
      M[Check: Report Version]
      N[Yes: Adjust Sales for Children]
      O[Fetch: Purchases per Category]
      P[Modify: Purchases using setSales]
      Q[Modify: Purchases using setSales2]
      R[Calculate: Total Purchases]
      S[Adjust: Purchases Percent from Total Purchases]
      T[Check: Report Version]
      U[Yes: Adjust Sales for Children]
      V[Fetch: DOE per Category]
      W[Set: All DOE]
      X[Calculate: Total DOE]
      Y[Fetch & Adjust: Labors]
      Z[Calculate: Sub Total Labors & Total Cash]
      AA[Calculate: Total Labors]
      AB[Calculate: Operational Profit & Prime Cost]
      AC[Check: API Authentication & Specific API Request]
      AD[Yes: Process & Return API Data]
      AE[No: Return View with Data]
      AF[End]

      A --> B
      B --> C
      C --> D
      D --> E
      E --> F
      F --> G
      G --> H
      G --> I
      H --> J
      I --> J
      J --> K
      K --> L
      J --> M
      M --> N
      N --> O
      M --> O
      O --> P
      O --> Q
      P --> R
      Q --> R
      R --> S
      R --> T
      T --> U
      U --> V
      R --> V
      V --> W
      W --> X
      R --> Y
      Y --> Z
      Z --> AA
      AA --> AB
      AB --> AC
      AC --> AD
      AC --> AE
      AD --> AF
      AE --> AF
```

#### `/report/detailed/purchase-report` - `GET`

```mermaid
graph TD
    A[Start: Detailed Purchase Report Generation]
    B[Initialize: Restaurant, Date]
    C[Check: Auth Guard & Report Version]
    D[Fetch: COGS & DOE Categories]
    E[Merge: COGS & DOE Categories]
    F[Add: Merged Categories to Request]
    G[Filter: Purchases using PurchaseReportFilter]
    H[Check: View Transfers Request]
    I[Yes: Fetch & Adjust Purchases with Transfers]
    J[Organize: Purchases by Category]
    K[Calculate: Total Data]
    L[Set: Chart Type to 'column']
    M[Check: Date Range in Request]
    N[Yes: Set From & To Dates]
    O[No: Null Dates]
    P[Set: RanOn Date]
    Q[Check: Auth Guard & View]
    R[Yes: Process & Return API Data]
    S[No: Return View with Data]
    T[End]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I
    G --> J
    I --> J
    J --> K
    K --> L
    L --> M
    M --> N
    M --> O
    N --> P
    O --> P
    P --> Q
    Q --> R
    Q --> S
    R --> T
    S --> T

```

#### `/report/guest-count` - `GET`

```mermaid
graph TD
    A[Start: Generate Guest Count Report]
    B[Initialize: Request Data]
    C[Initialize: PurchaseReportController & Restaurant]
    D[Check: If Departments in Request]
    E[Fetch: Department Sales Data]
    F[Fetch: Sale Guest Data]
    G[Organize: Data into Table]
    H[Calculate: Total Data]
    I[Set: Chart Type based on Request Group]
    J[Check: Date Range in Request]
    K[Yes: Set From & To Dates]
    L[No: Null Dates]
    M[Check: Auth Guard & Export]
    N[Yes: Process & Return API Data]
    O[No: Return View with Data]
    P[End]

    A --> B
    B --> C
    C --> D
    D --> E
    D --> F
    E --> G
    F --> G
    G --> H
    H --> I
    I --> J
    J --> K
    J --> L
    K --> M
    L --> M
    M --> N
    M --> O
    N --> P
    O --> P

```

#### `/report/inventory` - `GET`

```mermaid
graph TD
    A[Start: Run Inventory Report]
    B[Initialize: Dates & Restaurant]
    C[Fetch: Inventory Data]
    D[Fetch: Inventory Changes Data]
    E[Check: If Date Range in Request]
    F[Yes: Set From & To Dates]
    G[No: Null Dates]
    H[Check: Auth Guard & View]
    I[Yes: Process & Return API Data]
    J[No: Return View with Data]
    K[End]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    E --> G
    F --> H
    G --> H
    H --> I
    H --> J
    I --> K
    J --> K

```

#### `/report/labor` - `GET`

```mermaid
   graph TD
      A[Start: Generate Labor Report]
      B[Initialize: Data & Check Request]
      C[Retrieve: Restaurant & Date]
      D[Fetch: Labors Data]
      E[Check: If Request Data Available]
      F[Yes: Group and Table Labors]
      G[Calculate: Total Labors]
      H[Check: Date Range in Request]
      I[Yes: Set From & To Dates]
      J[No: Null Dates]
      K[Check: Auth Guard & View]
      L[Yes: Process & Return API Data]
      M[No: Return View with Data]
      N[End]

      A --> B
      B --> C
      C --> D
      D --> E
      E --> F
      F --> G
      G --> H
      H --> I
      H --> J
      I --> K
      J --> K
      K --> L
      K --> M
      L --> N
      M --> N
```

#### `/report/labor/detailed/category` - `GET`

```mermaid
   graph TD
    A[Start: Detailed Category Labor Report]
    B[Initialize: Data & Check Request]
    C[Retrieve: Restaurant & Date]
    D[Generate: Base Labor Report]
    E[Fetch: Labors Data by Category]
    F[Calculate: Fees & Totals]
    G[Check: Date Range in Request]
    H[Yes: Set From & To Dates]
    I[No: Null Dates]
    J[Check: Report Version & Discounts]
    K[Process: Discounts & Comps]
    L[Check: Auth Guard & View]
    M[Yes: Process & Return API Data]
    N[No: Return View with Data]
    O[End]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    G --> I
    H --> J
    I --> J
    J --> K
    K --> L
    L --> M
    L --> N
    M --> O
    N --> O
```

#### `/report/labor/efficiency` - `GET`

```mermaid
graph TD
    A[Start: Labor Efficiency Report]
    B[Initialize: Data & Check Request]
    C[Retrieve: Restaurant]
    D[Fetch: Labors Data]
    E[Group Labors by Request]
    F[Calculate: Labor Efficiency]
    G[Format: Labors for Table]
    H[Calculate: Totals]
    I[Set: Chart Type]
    J[Set: From & To Dates]
    K[Set: RanOn Date]
    L[Check: Auth Guard & View]
    M[Yes: Process & Return API Data]
    N[No: Return View with Data]
    O[End]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
    L --> M
    L --> N
    M --> O
    N --> O

```

#### `/report/labor/efficiency/export` - `POST`

```mermaid
graph TD
    A[Start: Export Labor Efficiency Report]
    B[Initialize & Get Request Data]
    C[Get Report Data from Generate function of /report/labor/efficiency]
    D[Set Filename]
    E[Check Export Type]
    F[Yes: PDF Export]
    G[No: Excel Export]
    H[End: Return File]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    E --> G
    F --> H
    G --> H


```

#### `/report/prime-cost-report` - `GET`

```mermaid
   graph TD
      A[Initialize variables, get current date and restaurant instance] --> B[Set or retrieve date range]
      B --> C[Fetch and process sales data]
      C --> D[Fetch and process purchase data using sales]
      D --> E[Fetch and process labor data]
      E --> F[Calculate contribution based on sales]
      F --> G[Compute prime cost and operational profit]
      G --> H[Calculate COGS percentage]
      H --> I[Compile data for API response or view]
```
