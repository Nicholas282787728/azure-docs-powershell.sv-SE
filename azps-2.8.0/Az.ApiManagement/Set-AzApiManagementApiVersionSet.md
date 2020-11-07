---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: a29713e91027ee6ca6e3cbc6390d63829fbb612c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745674"
---
# <span data-ttu-id="85227-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="85227-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="85227-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85227-102">SYNOPSIS</span></span>
<span data-ttu-id="85227-103">Uppdaterar en API-version i API-hanterings kontexten.</span><span class="sxs-lookup"><span data-stu-id="85227-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="85227-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85227-104">SYNTAX</span></span>

### <span data-ttu-id="85227-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="85227-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85227-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="85227-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85227-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85227-107">DESCRIPTION</span></span>

<span data-ttu-id="85227-108">Cmdleten **set-AzApiManagementApiVersionSet** ändrar en versions uppsättning för Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="85227-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="85227-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85227-109">EXAMPLES</span></span>

### <span data-ttu-id="85227-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="85227-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="85227-111">Det här kommandot uppdaterar en befintlig API-version med versions- `Header` och rubrik parameter `api-version` .</span><span class="sxs-lookup"><span data-stu-id="85227-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="85227-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85227-112">PARAMETERS</span></span>

### <span data-ttu-id="85227-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="85227-113">-ApiVersionSetId</span></span>
<span data-ttu-id="85227-114">Identifierare för den nya API-versionen.</span><span class="sxs-lookup"><span data-stu-id="85227-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85227-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="85227-115">-Context</span></span>
<span data-ttu-id="85227-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="85227-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="85227-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="85227-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85227-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85227-118">-DefaultProfile</span></span>
<span data-ttu-id="85227-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85227-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85227-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="85227-120">-Description</span></span>
<span data-ttu-id="85227-121">Beskrivning av API-versionen.</span><span class="sxs-lookup"><span data-stu-id="85227-121">Description of the Api Version set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85227-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="85227-122">-HeaderName</span></span>
<span data-ttu-id="85227-123">Huvudet som innehåller versions informationen.</span><span class="sxs-lookup"><span data-stu-id="85227-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="85227-124">Om versions schema rubrik väljs måste det här värdet anges.</span><span class="sxs-lookup"><span data-stu-id="85227-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85227-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85227-125">-InputObject</span></span>
<span data-ttu-id="85227-126">Instans av PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="85227-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="85227-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="85227-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85227-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="85227-128">-Name</span></span>
<span data-ttu-id="85227-129">Namnet på ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="85227-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="85227-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="85227-130">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85227-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85227-131">-PassThru</span></span>
<span data-ttu-id="85227-132">Om det här alternativet anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet typ som representerar den ändrade apiVersionSet att skrivas till output.</span><span class="sxs-lookup"><span data-stu-id="85227-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85227-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="85227-133">-QueryName</span></span>
<span data-ttu-id="85227-134">Värdet som innehåller versions informationen.</span><span class="sxs-lookup"><span data-stu-id="85227-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="85227-135">Om frågan versions schema är vald måste det här värdet anges.</span><span class="sxs-lookup"><span data-stu-id="85227-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85227-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="85227-136">-Scheme</span></span>
<span data-ttu-id="85227-137">Versions schema för att välja för uppsättningen API-versioner.</span><span class="sxs-lookup"><span data-stu-id="85227-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="85227-138">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="85227-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85227-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85227-139">-Confirm</span></span>
<span data-ttu-id="85227-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85227-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85227-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85227-141">-WhatIf</span></span>
<span data-ttu-id="85227-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85227-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85227-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85227-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85227-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85227-144">CommonParameters</span></span>
<span data-ttu-id="85227-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85227-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85227-146">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85227-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85227-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85227-147">INPUTS</span></span>

### <span data-ttu-id="85227-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="85227-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="85227-149">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="85227-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="85227-150">System. String</span><span class="sxs-lookup"><span data-stu-id="85227-150">System.String</span></span>

### <span data-ttu-id="85227-151">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="85227-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="85227-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85227-152">OUTPUTS</span></span>

### <span data-ttu-id="85227-153">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="85227-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="85227-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85227-154">NOTES</span></span>

## <span data-ttu-id="85227-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85227-155">RELATED LINKS</span></span>

[<span data-ttu-id="85227-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="85227-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="85227-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="85227-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="85227-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="85227-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
