---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262841"
---
# <span data-ttu-id="9b1db-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="9b1db-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="9b1db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b1db-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1db-103">Konstruera och utför HTTP-begäran till Azure Resource Management endast slut punkt</span><span class="sxs-lookup"><span data-stu-id="9b1db-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="9b1db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b1db-104">SYNTAX</span></span>

### <span data-ttu-id="9b1db-105">ByPath (standard)</span><span class="sxs-lookup"><span data-stu-id="9b1db-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b1db-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="9b1db-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b1db-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b1db-107">DESCRIPTION</span></span>
<span data-ttu-id="9b1db-108">Konstruera och utför HTTP-begäran till Azure Resource Management endast slut punkt</span><span class="sxs-lookup"><span data-stu-id="9b1db-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="9b1db-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b1db-109">EXAMPLES</span></span>

### <span data-ttu-id="9b1db-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b1db-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="9b1db-111">Hämta arbets yta för logganalys per sökväg</span><span class="sxs-lookup"><span data-stu-id="9b1db-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="9b1db-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b1db-112">PARAMETERS</span></span>

### <span data-ttu-id="9b1db-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9b1db-113">-ApiVersion</span></span>
<span data-ttu-id="9b1db-114">API-version</span><span class="sxs-lookup"><span data-stu-id="9b1db-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b1db-115">-AsJob</span></span>
<span data-ttu-id="9b1db-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9b1db-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1db-117">-DefaultProfile</span></span>
<span data-ttu-id="9b1db-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-119">-Metod</span><span class="sxs-lookup"><span data-stu-id="9b1db-119">-Method</span></span>
<span data-ttu-id="9b1db-120">Http-metod</span><span class="sxs-lookup"><span data-stu-id="9b1db-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b1db-121">-Name</span></span>
<span data-ttu-id="9b1db-122">lista över mål resurs namn</span><span class="sxs-lookup"><span data-stu-id="9b1db-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-123">-Path</span><span class="sxs-lookup"><span data-stu-id="9b1db-123">-Path</span></span>
<span data-ttu-id="9b1db-124">Mål Sök väg</span><span class="sxs-lookup"><span data-stu-id="9b1db-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-125">-Nyttolast</span><span class="sxs-lookup"><span data-stu-id="9b1db-125">-Payload</span></span>
<span data-ttu-id="9b1db-126">Nytto last för JSON-format</span><span class="sxs-lookup"><span data-stu-id="9b1db-126">JSON format payload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1db-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b1db-128">Namn på mål resurs grupp</span><span class="sxs-lookup"><span data-stu-id="9b1db-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="9b1db-129">-ResourceProviderName</span></span>
<span data-ttu-id="9b1db-130">Namn på mål resurs leverantör</span><span class="sxs-lookup"><span data-stu-id="9b1db-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9b1db-131">-ResourceType</span></span>
<span data-ttu-id="9b1db-132">Lista över mål resurs typer</span><span class="sxs-lookup"><span data-stu-id="9b1db-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b1db-133">-SubscriptionId</span></span>
<span data-ttu-id="9b1db-134">ID för mål prenumeration</span><span class="sxs-lookup"><span data-stu-id="9b1db-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b1db-135">-Confirm</span></span>
<span data-ttu-id="9b1db-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b1db-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b1db-137">-WhatIf</span></span>
<span data-ttu-id="9b1db-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b1db-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b1db-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b1db-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1db-140">CommonParameters</span></span>
<span data-ttu-id="9b1db-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b1db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1db-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b1db-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1db-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b1db-143">INPUTS</span></span>

### <span data-ttu-id="9b1db-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9b1db-144">System.string</span></span>

## <span data-ttu-id="9b1db-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b1db-145">OUTPUTS</span></span>

### <span data-ttu-id="9b1db-146">Microsoft. Azure. commands. Profile. Models. PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="9b1db-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="9b1db-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b1db-147">NOTES</span></span>

## <span data-ttu-id="9b1db-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b1db-148">RELATED LINKS</span></span>
