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

#### `/report/labor/export` - `POST`

```mermaid
graph TD
    A[Start: Export Labor Report]
    B[Initialize & Get Request Data]
    C[Check Report Type]
    D[Detailed Category Report]
    E[Detailed Job Report]
    F[Default: Labor Report]
    G[Set Filename and Report Name]
    H[Check Export Type]
    I[PDF Export]
    J[Excel Export]
    K[End: Return File]

    A --> B
    B --> C
    C --report_type: detailed_category--> D
    C --report_type: detailed_job--> E
    C --report_type: default--> F
    D --> G
    E --> G
    F --> G
    G --> H
    H --type: pdf--> I
    H --type: excel--> J
    I --> K
    J --> K

```

#### `/report/monthly-overview` - `GET`

```mermaid
   graph TD
    A[Start: Monthly Overview Report]
    B[Get Request Parameters]
    C[Initialize Restaurant]
    D[Retrieve Monthly Data]
    E[Retrieve Sales Data]
    F[Retrieve COGS Purchase Data]
    G[Check If Operating Expense is Set]
    H[Retrieve DOE Purchase Data]
    I[Check If Labor Setting is Enabled]
    J[Retrieve Labor Data]
    K[Set Date Range for Report]
    L[Check If Request is from API and not a View]
    M[Return Data for API]
    N[Return View for Web]
    O[End: Report Generated]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --Yes--> H
    H --> I
    G --No--> I
    I --Yes--> J
    J --> K
    I --No--> K
    K --> L
    L --Yes--> M
    M --> O
    L --No--> N
    N --> O

```

#### `/report/operational-profit` - `GET`

```mermaid
   graph TD
    A[Start: Operational Profit Report]
    B[Initialize PrimeCostReportController]
    C[Check if Request is from API]
    D[Execute the run method of PrimeCostReportController]
    E[Modify export links for API]
    F[Return Data for API]
    G[Execute the run method of PrimeCostReportController for Web]
    H[Get Data for Web]
    I[Return View for Web]
    J[End: Report Generated]

    A --> B
    B --> C
    C --Yes--> D
    D --> E
    E --> F
    F --> J
    C --No--> G
    G --> H
    H --> I
    I --> J

```

#### `/report/options` - `GET`

```mermaid
graph TD
    A[Start: Fetch Report Options]
    B[Check for new_category in request]
    C[Check for new_comps in request]
    D[Get Range]
    E[Get Groups]
    F[Get Categories]
    G[Get Comps]
    H[Get Years]
    I[Get Periods]
    J[Get Weeks]
    K[Get Traffics]
    L[Get Reasons]
    M[Get Start Week]
    N[Get Inventory Types]
    O[Get Months]
    P[Get COGS Category]
    Q[Get Departments]
    R[Get Vendors]
    S[Get Labor Categories]
    T[Get Jobs]
    U[Flatten Categories]
    V[Flatten Groups]
    W[Flatten Comps]
    X[End: Return Options]

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
    M --> N
    N --> O
    O --> P
    P --> Q
    Q --> R
    R --> S
    S --> T
    T --> U
    U --> V
    V --> W
    W --> X
```

#### `/report/overview-report/export` - `POST`

```mermaid
graph TD
    A[Start: Export Overview Report]
    B[Run Overview Report with Request Data]
    C[Get Data from Run Function]
    D[Set Export Flag in Data]
    E[Get Chart Data from Request]
    F[Prepare PDF Content View]
    G[Prepare PDF Header View]
    H[Load PDF with Content]
    I[Set Paper Size to Letter]
    J[Set Header Spacing]
    K[Set Header HTML]
    L[Set Footer HTML]
    M[Define File Name]
    N[End: Download PDF File]

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
    M --> N
```

#### `/report/per-person-avg` - `GET`

```mermaid
graph TD
    A[Start: Generate Per Person Avg Report]
    B[Get Restaurant Details]
    C[Check if Request is Defined]
    D[Initialize PurchaseReportController]
    E[Check if Departments is Defined in Request]
    F[Get Department Sale Data]
    G[Get Sale Guest Data with Comps]
    H[Process Sale Guest Data with Comps]
    I[Calculate Total Count]
    J[Get Total Data for Items]
    K[Format Table with 'Average Sale']
    L[Calculate Total Data]
    M[Define Chart Type Based on Group in Request]
    N[Check if Request is from API and Not an Export]
    O[Return Data]
    P[End: Return View with Data]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    E --> G
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
    L --> M
    M --> N
    N --> O
    N --> P
```

#### `/report/prime-cost-report` - `GET`

```mermaid
graph TD
    A[Start: Prime Cost Report]
    B[Get Current Date and Restaurant]
    C[Initialize Variables]
    D[Based on 'group' parameter from request]
    E1[Process Weekly Reports]
    E2[Process Monthly Reports]
    E3[Process Daily Reports for Specific Days Mon-Sun]
    E4[Process Yearly Reports]
    E5[Process Default/Daily Reports]
    F[Construct Chart Data]
    G[Check if Request is from API]
    H1[Return Data for API]
    H2[Return View for Web]
    I[End: Report Generated]

    A --> B
    B --> C
    C --> D
    D --> E1
    D --> E2
    D --> E3
    D --> E4
    D --> E5
    E1 --> F
    E2 --> F
    E3 --> F
    E4 --> F
    E5 --> F
    F --> G
    G --Yes--> H1
    G --No--> H2
    H1 --> I
    H2 --> I

```

#### `/report/prime-cost-report/export` - `POST`

```mermaid
graph TD
    A[Start: Prime Cost Report Export]
    B[Check if Request is from API]
    C1[Parse query parameters from request]
    C2[Continue]
    D[Based on 'type' parameter from request]
    E1[Generate PDF Report]
    E2[Generate Excel Report]
    F[Based on profit_report attribute in request]
    G1[Operational Profit Report]
    G2[Prime Cost Report]
    H[Set PDF Settings]
    I[End: Download PDF Report]

    A --> B
    B --Yes--> C2
    B --No--> C1
    C1 --> C2
    C2 --> D
    D --> E1
    D --> E2
    E1 --> F
    F --Yes--> G1
    F --No--> G2
    G1 --> H
    G2 --> H
    H --> I

```

#### `/report/prime-cost-report/export/detailed` - `POST`

```mermaid
graph TD
    A[Start: Prime Cost Report Detailed Export]
    B[Check if Request is from API or has 'query' attribute]
    C1[Parse query parameters from request]
    C2[Continue]
    D[Based on 'type' parameter from request]
    E1[Generate Detailed PDF Report]
    E2[Generate Detailed Excel Report]
    F[Get data for report]
    G[Check if profit_report attribute is set in request]
    H1[Operational Profit Detailed Report]
    H2[Prime Cost Inventory Report]
    H3[Prime Cost Detailed Report]
    I[Set PDF Settings]
    J[End: Download PDF Report]

    A --> B
    B --Yes--> C2
    B --No--> C1
    C1 --> C2
    C2 --> D
    D --> E1
    D --> E2
    E1 --> F
    F --> G
    G --Yes--> H1
    G --prime_cost_inventory_report is set--> H2
    G --No--> H3
    H1 --> I
    H2 --> I
    H3 --> I
    I --> J
```

#### `/report/profit-loss` - `GET`

```mermaid
graph TD
    A[Start: Profit & Loss Report]
    B[Initialize start and end dates]
    C{Check if from date is provided in request}
    D1[Set default date to start of last month]
    D2[Convert from and to from request to Carbon dates]
    E[Get range from start and end dates]
    F[Calculate COGS Sales]
    G[Calculate Purchases]
    H[Calculate DOE]
    I[Calculate Expenses]
    J[Calculate Labor]
    K[Compute Prime Cost, Controllable Expense, Total Expense, and Operational Profit]
    L{Check if request is from API and not for view}
    M1[Prepare API data response]
    M2[Generate Report View]
    N[End: Return API data]
    O[End: Return Report View]

    A --> B
    B --> C
    C --No--> D1
    C --Yes--> D2
    D1 --> E
    D2 --> E
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
    L --Yes--> M1
    L --No--> M2
    M1 --> N
    M2 --> O

    subgraph salesCogs
        F --> P[Get COGS Categories and their Sales]
        P --> Q[Compute Sum and Percentage of Sales]
    end
```

#### `/report/profit-loss/export` - `POST`

```mermaid
graph TD
    A[Start: Export Profit & Loss Report]
    B{Check if request is from API}
    C1[Invoke index for API data]
    C2[Invoke index for View data]
    D[Prepare the data for PDF export]
    E[Load PDF with the content]
    F[Set PDF options]
    G[End: Return downloaded PDF]

    A --> B
    B --API--> C1
    B --Not API--> C2
    C1 --> D
    C2 --> D
    D --> E
    E --> F
    F --> G

    subgraph index
        C1 --> I1[Initialize start and end dates]
        C2 --> I1
        I1 --> I2[Compute range]
        I2 --> I3[Calculate COGS Sales, Purchases, DOE, Expenses, and Labor]
        I3 --> I4[Compute Prime Cost and related metrics]
        I4 --> I5[Check if Discounts table is needed]
        I5 --> I6[Get Sales Data, Calculate COGS and other metrics]
    end
```

#### `/report/purchase-report` - `GET`

```mermaid
graph TD
    A[Start: Generate Purchase Report]
    B{Check for restaurant}
    C[Set restaurant]
    D{Check if request is from API and has report_version}
    E[Check for request categories]
    F[Include Category Children]
    G[Initialize Purchase Filters]
    H[Get Purchases]
    I[Apply Expenses]
    J{Check if view_transfers input is set}
    K[Apply Transfers]
    L[Sort and Serialize Purchases]
    M[Calculate Table]
    N[Calculate Totals]
    O[Set Chart Type]
    P{Check for date range in request}
    Q[Set Dates]
    R[Return View]
    S[End: Return API data]

    A --> B
    B --No restaurant--> C
    C --> D
    B --Restaurant present--> D
    D --API request with report_version--> E
    D --Not an API request with report_version--> G
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J
    J --view_transfers set--> K
    J --view_transfers not set--> L
    K --> L
    L --> M
    M --> N
    N --> O
    O --> P
    P --Date range provided--> Q
    P --No date range provided--> R
    Q --> R
    R --API request with no view--> S
    R --Not an API request--> END[Return View]
    S --> END[Return Data as API Response]

    subgraph expenses
        I --> X1[Initialize date range]
        X1 --> X2[Return purchases]
    end
```

#### `/report/purchase/export` - `POST`

```mermaid
graph TD
    A[Start: Export Purchase Report]
    B[Retrieve all request data]
    C{Check if detailed report requested}
    D[Generate Detailed Report]
    E[Generate Standard Report]
    F[Set Filename]
    G{Check Report Type}
    H[Generate PDF]
    I[Generate Excel]
    J[End]

    A --> B
    B --> C
    C --Yes--> D
    C --No--> E
    D --> F
    E --> F
    F --> G
    G --PDF--> H
    G --Excel--> I
    H --> J
    I --> J

    subgraph DetailedReportFlow
        D --> X1[Set Restaurant if not set]
        X1 --> X2[Set Date if not set]
        X2 --> X3{Check if request is from API with report_version}
        X3 --Yes--> X4[Retrieve categories and filters]
        X4 --> X5[Get Purchases by filter]
        X3 --No--> X5
        X5 --> X6{Check if view_transfers is set in request}
        X6 --Yes--> X7[Apply Transfers]
        X7 --> X8[Serialize and Categorize Purchases]
        X6 --No--> X8
        X8 --> X9[Calculate Totals]
        X9 --> X10[Set Chart Type and Retrieve other data]
    end

```

#### `/report/purchase/vendor` - `GET`

```mermaid
graph TD
    A[Start: Run Purchase Vendor Report]
    B[Set default restaurant if not present]
    C[Set default date if not present]
    D[Fetch invoices per vendor]
    E[Group invoices by vendor ID]
    F[Initialize chart and sum]
    G[For each vendor in vendors]
    H[Find Vendor from Vendor ID]
    I[Calculate total for each purchase]
    J[If Vendor exists, add to chart]
    K[Update Sum]
    L[Set date range]
    M[Format invoice date]
    N[If request is from API and not view]
    O[Prepare data for API]
    P[Return data]
    Q[Else, prepare data for view]
    R[Return view]

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
    K -->|For each vendor| G
    K --> L
    L --> M
    M --> N
    N --> O
    O --> P
    N --> Q
    Q --> R
```

#### `/report/purchase/vendor/export` - `POST`

```mermaid
graph TD
    A[Start: Export Purchase Vendor Report]
    B{Check request type}
    C[Export as PDF]
    D[Prepare Data for PDF]
    E[Load PDF view and Download]
    F[Export as Excel]
    G[Prepare Data for Excel]
    H[Format Excel using excel_format]
    I[End]

    A --> B
    B --PDF--> C
    C --> D
    D --> E
    E --> I
    B --Excel--> F
    F --> G
    G --> H
    H --> I

```

#### `/report/sales-daily` - `GET`

```mermaid
graph TD
    A[Start: Sales Daily Report]
    B{Check for restaurant}
    C[Use passed restaurant]
    D[Use default restaurant]
    E[Initialize variables]
    F{Check if API request}
    G[Process Categories for COGS]
    H{Detailed Request Check}
    I{Traffic Report Check}
    J[Set Detailed Report Name]
    K[Set Traffic Report Name]
    L[Set Sales Report Name]
    M{Detailed Report Check Back Link}
    N[Set Detailed Back Link]
    O[Set Back Link]
    P{Is request scheduled?}
    Q[Process Sales Data]
    R[Process Sales Chart Data]
    S{Detailed Report Check}
    T[Format Sales Data]
    U{Check for API Request}
    V[Prepare API Response]
    W[Return View]

    A --> B
    B --> |Yes| C
    B --> |No| D
    C --> E
    D --> E
    E --> F
    F --> |Yes| G
    F --> |No| H
    G --> H
    H --> |Yes| I
    H --> |No| I
    I --> |Yes| K
    I --> |No| J
    K --> L
    J --> L
    L --> M
    M --> |Yes| N
    M --> |No| O
    N --> P
    O --> P
    P --> |No| Q
    Q --> R
    R --> S
    S --> |Yes| T
    S --> |No| U
    T --> U
    U --> V
    V --> W
```

#### `/report/sales-daily/export` - `POST`

```mermaid
graph TD
    start((Start: Sales Daily Export))
    departmentCheck{Check 'sales_by_department' input}
    salesDataCall[Call: sales_daily function]
    checkExportType{Check export type}
    pdfExport[Export PDF]
    excelExport[Export Excel]

    subgraph sales_daily_function [Sales Daily Function]
    A[Start: Sales Daily Report]
    B[Initialize variables]
    C[Check API guard and report_version]
    D[Check 'detailed' input]
    E[Set Report Name based on Department]
    F[Set Report Name based on Traffic Report]
    G[Set Default Sales Report Name]
    H[Check 'detailed' input for Back Link]
    I[Set Back Link]
    J[Check if Request is Scheduled]
    K[Process Sales Data]
    L[Check 'detailed' and 'categories']
    M[Set Sales Data]
    N[Return API Data]
    O[Return View]
    end

    start --> departmentCheck
    departmentCheck --> salesDataCall
    salesDataCall --> checkExportType
    N --> checkExportType
    checkExportType --> |pdf| pdfExport
    checkExportType --> |excel| excelExport

    salesDataCall --> A
    A --> B
    B --> C
    C --> D
    D --> |Yes| E
    D --> |No| F
    F --> G
    G --> H
    H --> |No| I
    I --> J
    J --> |No| K
    K --> L
    L --> M
    M --> N
    N --> O

```

#### `/report/sales/guest_count/export` - `POST`

```mermaid
graph TD
    start((Start: Guest Count Export))
    requestData[Get request data]
    callGenerate[Call: generate function]
    checkExportType{Check export type}
    pdfExport[Export PDF]
    excelExport[Export Excel]

    subgraph generate_function [Generate Function]
    A[Start: Generate Report]
    B[Initialize variables]
    C[Check if request is null]
    D[Initialize Restaurant]
    E[Check for 'departments' in request]
    F[Get Department Sale Data]
    G[Get Sale Guest Data]
    H[Process Table Data]
    I[Calculate Totals]
    J[Set Chart Type]
    K[Check if API Guard & Not Export]
    L[Prepare API Data]
    M[Return View]
    end

    start --> requestData
    requestData --> callGenerate
    callGenerate --> checkExportType
    L --> checkExportType
    checkExportType --> |pdf| pdfExport
    checkExportType --> |excel| excelExport

    callGenerate --> A
    A --> B
    B --> C
    C --> D
    D --> E
    E --> |Yes| F
    E --> |No| G
    F --> H
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
    L --> M
```

#### `/report/sales/per_person/export` - `POST`

```mermaid
graph TD
    start((Start: Per Person Export))
    requestData[Get request data]
    callGenerate[Call: generate function]
    checkExportType{Check export type}
    pdfExport[Export PDF]
    excelExport[Export Excel]

    subgraph generate_function [Generate Function]
    A[Start: Generate Report]
    B[Initialize Restaurant]
    C[Get Request Data if null]
    D[Initialize PurchaseReportController]
    E[Check if 'departments' in request]
    F[Get Department Sale Data]
    G[Get Sale Guest Data]
    H[Process Sale Guest Data with Comps]
    I[Calculate Totals for Items]
    J[Process Table Data]
    K[Calculate Overall Totals]
    L[Set Chart Type]
    M[Check if API Guard & Not Export]
    N[Prepare API Data]
    O[Return View]
    end

    start --> requestData
    requestData --> callGenerate
    callGenerate --> checkExportType
    N --> checkExportType
    checkExportType --> |pdf| pdfExport
    checkExportType --> |excel| excelExport

    callGenerate --> A
    A --> B
    B --> C
    C --> D
    D --> E
    E --> |Yes| F
    E --> |No| G
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
    L --> M
    M --> N
    N --> O
```

#

---

#### `/partner-company/` - `POST`

```mermaid
graph TD
    start((Start: Store Partner Company))
    createCompany[Create Partner Company]
    syncCompanyRestaurants[Sync Restaurants to Company]
    callSaveUsers[Call: _saveNewUsers function]
    syncCompanyUsers[Sync Users to Company]
    returnResponse[Return Response]

    subgraph saveNewUsers_function [_saveNewUsers Function]
    A[Start: Save New Users]
    B[Initialize User IDs]
    C{Iterate over Users}
    D[Check if New User]
    E[Create New User]
    F[Disable Restaurant Access]
    G[Send Activation Email]
    H[Add ID to List]
    I[Check if Existing New User]
    J[Find and Update User]
    K[Send Partner User Email]
    L[Log Account Activity]
    M[Add ID to List]
    N[Check if Existing User]
    O[Add ID to List]
    P[End Iteration]
    end

    start --> createCompany
    createCompany --> syncCompanyRestaurants
    syncCompanyRestaurants --> callSaveUsers
    callSaveUsers --> syncCompanyUsers
    syncCompanyUsers --> returnResponse

    callSaveUsers --> A
    A --> B
    B --> C
    C --> |For each User| D
    D --> |New User| E
    E --> F
    F --> G
    G --> H
    H --> P
    D --> |Existing New User| I
    I --> J
    J --> K
    K --> L
    L --> M
    M --> P
    D --> |Existing User| N
    N --> O
    O --> P
    P --> |Next User| C
    C --> |End of Users| returnResponse

```

#### `/partner-company/{company}` - `GET`

```mermaid
graph TD
    A[Start: Show Partner Company]
    B{Check if User is Partner Admin}
    C{Check if Company ID matches User's Partner Company ID}
    D[Abort with 403]
    E[Return Company Data]

    A --> B
    B --> |Yes| C
    C --> |No| D
    C --> |Yes| E
    B --> |No| E
```

#

---

#### `/report-suggestion/ajax` - `GET`

```mermaid
graph TD
    A[Start: Ajax Call]
    B{Check if User Role is 1 Admin}
    C[Set Report Suggestion Query for Admin]
    D[Set Report Suggestion Query for User]
    E{Sort Direction Check}
    F[Descending Order]
    G[Ascending Order]
    H{Keyword Check}
    I[Apply Keyword Filter]
    J{Filter Parameter Check}
    K[Apply Filters]
    L{Check if User is from API Guard}
    M[Apply Pagination]
    N[Datatables Transformation]
    O[End: Return Datatables]

    A --> B
    B --> |Yes| C
    B --> |No| D
    C --> E
    D --> E
    E --> |Descending| F
    E --> |Ascending| G
    F --> H
    G --> H
    H --> |Keyword exists| I
    I --> J
    H --> |No Keyword| J
    J --> |Filters exist| K
    K --> L
    J --> |No Filters| L
    L --> |API Guard User| M
    M --> N
    L --> |Non-API Guard User| N
    N --> O
```
