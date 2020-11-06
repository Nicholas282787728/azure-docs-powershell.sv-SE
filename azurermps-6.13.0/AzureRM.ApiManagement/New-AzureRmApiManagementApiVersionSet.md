---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: e10b91994bdb7351a7154d04cb7de3231ed87a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575384"
---
# <span data-ttu-id="4a28e-101">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a28e-101">New-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="4a28e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a28e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a28e-103">Skapar en API-version.</span><span class="sxs-lookup"><span data-stu-id="4a28e-103">Creates an API Version Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a28e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a28e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -Name <String> -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a28e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a28e-105">DESCRIPTION</span></span>
<span data-ttu-id="4a28e-106">Cmdleten **New-AzureRmApiManagementApiVersionSet** skapar en API-version inställd i Azure API Management-kontexten.</span><span class="sxs-lookup"><span data-stu-id="4a28e-106">The **New-AzureRmApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="4a28e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a28e-107">EXAMPLES</span></span>

### <span data-ttu-id="4a28e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4a28e-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

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

<span data-ttu-id="4a28e-109">Det här kommandot skapar en API-version som anger vilken versions- `Query` och Frågeparametern som är `api-version` .</span><span class="sxs-lookup"><span data-stu-id="4a28e-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="4a28e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a28e-110">PARAMETERS</span></span>

### <span data-ttu-id="4a28e-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="4a28e-111">-ApiVersionSetId</span></span>
<span data-ttu-id="4a28e-112">Identifierare för den nya API-versionen.</span><span class="sxs-lookup"><span data-stu-id="4a28e-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="4a28e-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="4a28e-113">This parameter is optional.</span></span>
<span data-ttu-id="4a28e-114">Om inget anges genereras en identifierare.</span><span class="sxs-lookup"><span data-stu-id="4a28e-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="4a28e-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4a28e-115">-Context</span></span>
<span data-ttu-id="4a28e-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4a28e-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4a28e-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4a28e-117">This parameter is required.</span></span>

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

### <span data-ttu-id="4a28e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a28e-118">-DefaultProfile</span></span>
<span data-ttu-id="4a28e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a28e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a28e-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4a28e-120">-Description</span></span>
<span data-ttu-id="4a28e-121">Beskrivning av API-versionen.</span><span class="sxs-lookup"><span data-stu-id="4a28e-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="4a28e-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="4a28e-122">-HeaderName</span></span>
<span data-ttu-id="4a28e-123">Huvudet som innehåller versions informationen.</span><span class="sxs-lookup"><span data-stu-id="4a28e-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="4a28e-124">Om versions schema rubrik väljs måste det här värdet anges.</span><span class="sxs-lookup"><span data-stu-id="4a28e-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="4a28e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a28e-125">-Name</span></span>
<span data-ttu-id="4a28e-126">Namnet på ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="4a28e-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="4a28e-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4a28e-127">This parameter is required.</span></span>

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

### <span data-ttu-id="4a28e-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="4a28e-128">-QueryName</span></span>
<span data-ttu-id="4a28e-129">Värdet som innehåller versions informationen.</span><span class="sxs-lookup"><span data-stu-id="4a28e-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="4a28e-130">Om du väljer versions schema fråga måste det här värdet anges.</span><span class="sxs-lookup"><span data-stu-id="4a28e-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="4a28e-131">-Schema</span><span class="sxs-lookup"><span data-stu-id="4a28e-131">-Scheme</span></span>
<span data-ttu-id="4a28e-132">Versions schema för att välja för uppsättningen API-versioner.</span><span class="sxs-lookup"><span data-stu-id="4a28e-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="4a28e-133">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4a28e-133">This parameter is required.</span></span>

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

### <span data-ttu-id="4a28e-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a28e-134">-Confirm</span></span>
<span data-ttu-id="4a28e-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a28e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a28e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a28e-136">-WhatIf</span></span>
<span data-ttu-id="4a28e-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a28e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a28e-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a28e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a28e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a28e-139">CommonParameters</span></span>
<span data-ttu-id="4a28e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a28e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a28e-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a28e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a28e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a28e-142">INPUTS</span></span>

### <span data-ttu-id="4a28e-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4a28e-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="4a28e-144">Parametrar: kontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4a28e-144">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="4a28e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4a28e-145">System.String</span></span>

### <span data-ttu-id="4a28e-146">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="4a28e-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="4a28e-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a28e-147">OUTPUTS</span></span>

### <span data-ttu-id="4a28e-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a28e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="4a28e-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a28e-149">NOTES</span></span>

## <span data-ttu-id="4a28e-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a28e-150">RELATED LINKS</span></span>

[<span data-ttu-id="4a28e-151">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a28e-151">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="4a28e-152">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a28e-152">Remove-AzureRmApiManagementApiVersionSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="4a28e-153">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4a28e-153">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
