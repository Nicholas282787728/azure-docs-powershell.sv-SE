---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525046"
---
# <span data-ttu-id="1db66-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1db66-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1db66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1db66-102">SYNOPSIS</span></span>
<span data-ttu-id="1db66-103">Skapar en API-version.</span><span class="sxs-lookup"><span data-stu-id="1db66-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="1db66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1db66-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1db66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1db66-105">DESCRIPTION</span></span>
<span data-ttu-id="1db66-106">Cmdleten **New-AzApiManagementApiVersionSet** skapar en API-version inställd i Azure API Management-kontexten.</span><span class="sxs-lookup"><span data-stu-id="1db66-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="1db66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1db66-107">EXAMPLES</span></span>

### <span data-ttu-id="1db66-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1db66-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="1db66-109">Det här kommandot skapar en API-version som anger vilken versions- `Query` och Frågeparametern som är `api-version` .</span><span class="sxs-lookup"><span data-stu-id="1db66-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="1db66-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1db66-110">PARAMETERS</span></span>

### <span data-ttu-id="1db66-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1db66-111">-ApiVersionSetId</span></span>
<span data-ttu-id="1db66-112">Identifierare för den nya API-versionen.</span><span class="sxs-lookup"><span data-stu-id="1db66-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="1db66-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1db66-113">This parameter is optional.</span></span>
<span data-ttu-id="1db66-114">Om inget anges genereras en identifierare.</span><span class="sxs-lookup"><span data-stu-id="1db66-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="1db66-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1db66-115">-Context</span></span>
<span data-ttu-id="1db66-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1db66-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1db66-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="1db66-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1db66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db66-118">-DefaultProfile</span></span>
<span data-ttu-id="1db66-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1db66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1db66-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1db66-120">-Description</span></span>
<span data-ttu-id="1db66-121">Beskrivning av API-versionen.</span><span class="sxs-lookup"><span data-stu-id="1db66-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="1db66-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="1db66-122">-HeaderName</span></span>
<span data-ttu-id="1db66-123">Huvudet som innehåller versions informationen.</span><span class="sxs-lookup"><span data-stu-id="1db66-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="1db66-124">Om versions schema rubrik väljs måste det här värdet anges.</span><span class="sxs-lookup"><span data-stu-id="1db66-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="1db66-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="1db66-125">-Name</span></span>
<span data-ttu-id="1db66-126">Namnet på ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="1db66-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="1db66-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="1db66-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1db66-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="1db66-128">-QueryName</span></span>
<span data-ttu-id="1db66-129">Värdet som innehåller versions informationen.</span><span class="sxs-lookup"><span data-stu-id="1db66-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="1db66-130">Om frågan versions schema är vald måste det här värdet anges.</span><span class="sxs-lookup"><span data-stu-id="1db66-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="1db66-131">-Schema</span><span class="sxs-lookup"><span data-stu-id="1db66-131">-Scheme</span></span>
<span data-ttu-id="1db66-132">Versions schema för att välja för uppsättningen API-versioner.</span><span class="sxs-lookup"><span data-stu-id="1db66-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="1db66-133">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="1db66-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1db66-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1db66-134">-Confirm</span></span>
<span data-ttu-id="1db66-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1db66-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1db66-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db66-136">-WhatIf</span></span>
<span data-ttu-id="1db66-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1db66-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1db66-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1db66-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1db66-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db66-139">CommonParameters</span></span>
<span data-ttu-id="1db66-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db66-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db66-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1db66-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db66-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1db66-142">INPUTS</span></span>

### <span data-ttu-id="1db66-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1db66-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1db66-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1db66-144">System.String</span></span>

### <span data-ttu-id="1db66-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="1db66-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="1db66-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1db66-146">OUTPUTS</span></span>

### <span data-ttu-id="1db66-147">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1db66-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1db66-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1db66-148">NOTES</span></span>

## <span data-ttu-id="1db66-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1db66-149">RELATED LINKS</span></span>

[<span data-ttu-id="1db66-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1db66-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1db66-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1db66-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1db66-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1db66-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)