---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 5d9bc89eb2d4188b7b2903bee7a8b0a44bec1216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579099"
---
# <span data-ttu-id="4a3a3-101">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a3a3-101">Set-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="4a3a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a3a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3a3-103">Uppdaterar en API-version i API-hanterings kontexten.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-103">Updates an API Version Set in the API Management Context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a3a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a3a3-104">SYNTAX</span></span>

### <span data-ttu-id="4a3a3-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="4a3a3-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-Name <String>] [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a3a3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a3a3-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a3a3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a3a3-107">DESCRIPTION</span></span>

<span data-ttu-id="4a3a3-108">Cmdleten **set-AzureRmApiManagementApiVersionSet** ändrar en versions uppsättning för Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-108">The **Set-AzureRmApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="4a3a3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a3a3-109">EXAMPLES</span></span>

### <span data-ttu-id="4a3a3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4a3a3-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="4a3a3-111">Det här kommandot uppdaterar en befintlig API-version med versions- `Header` och rubrik parameter `api-version` .</span><span class="sxs-lookup"><span data-stu-id="4a3a3-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="4a3a3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a3a3-112">PARAMETERS</span></span>

### <span data-ttu-id="4a3a3-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="4a3a3-113">-ApiVersionSetId</span></span>
<span data-ttu-id="4a3a3-114">Identifierare för den nya API-versionen.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="4a3a3-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4a3a3-115">-Context</span></span>
<span data-ttu-id="4a3a3-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4a3a3-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3a3-118">-DefaultProfile</span></span>
<span data-ttu-id="4a3a3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a3-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4a3a3-120">-Description</span></span>
<span data-ttu-id="4a3a3-121">Beskrivning av API-versionen.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="4a3a3-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="4a3a3-122">-HeaderName</span></span>
<span data-ttu-id="4a3a3-123">Huvudet som innehåller versions informationen.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="4a3a3-124">Om versions schema rubrik väljs måste det här värdet anges.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="4a3a3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a3a3-125">-InputObject</span></span>
<span data-ttu-id="4a3a3-126">Instans av PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="4a3a3-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-127">This parameter is required.</span></span>

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

### <span data-ttu-id="4a3a3-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a3a3-128">-Name</span></span>
<span data-ttu-id="4a3a3-129">Namnet på ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="4a3a3-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a3a3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a3a3-131">-PassThru</span></span>
<span data-ttu-id="4a3a3-132">Om det här alternativet anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet typ som representerar den ändrade apiVersionSet att skrivas till output.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="4a3a3-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="4a3a3-133">-QueryName</span></span>
<span data-ttu-id="4a3a3-134">Värdet som innehåller versions informationen.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="4a3a3-135">Om du väljer versions schema fråga måste det här värdet anges.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-135">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="4a3a3-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="4a3a3-136">-Scheme</span></span>
<span data-ttu-id="4a3a3-137">Versions schema för att välja för uppsättningen API-versioner.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="4a3a3-138">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a3a3-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a3a3-139">-Confirm</span></span>
<span data-ttu-id="4a3a3-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a3a3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a3a3-141">-WhatIf</span></span>
<span data-ttu-id="4a3a3-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a3a3-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a3a3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3a3-144">CommonParameters</span></span>
<span data-ttu-id="4a3a3-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a3a3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3a3-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a3a3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3a3-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a3a3-147">INPUTS</span></span>

### <span data-ttu-id="4a3a3-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4a3a3-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4a3a3-149">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a3a3-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="4a3a3-150">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4a3a3-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4a3a3-151">System. String</span><span class="sxs-lookup"><span data-stu-id="4a3a3-151">System.String</span></span>

### <span data-ttu-id="4a3a3-152">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="4a3a3-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="4a3a3-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a3a3-153">OUTPUTS</span></span>

### <span data-ttu-id="4a3a3-154">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a3a3-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="4a3a3-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a3a3-155">NOTES</span></span>

## <span data-ttu-id="4a3a3-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a3a3-156">RELATED LINKS</span></span>

[<span data-ttu-id="4a3a3-157">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a3a3-157">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="4a3a3-158">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a3a3-158">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="4a3a3-159">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a3a3-159">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
