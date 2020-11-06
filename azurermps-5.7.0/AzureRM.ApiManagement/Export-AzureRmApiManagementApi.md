---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 3985f393e642645ddf9f023756e78db20074c214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586447"
---
# <span data-ttu-id="73934-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="73934-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="73934-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73934-102">SYNOPSIS</span></span>
<span data-ttu-id="73934-103">Exporterar ett API till en fil.</span><span class="sxs-lookup"><span data-stu-id="73934-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73934-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73934-104">SYNTAX</span></span>

### <span data-ttu-id="73934-105">ExportToPipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="73934-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73934-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="73934-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73934-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73934-107">DESCRIPTION</span></span>
<span data-ttu-id="73934-108">Cmdleten **export-AzureRmApiManagementApi** exporterar ett API för Azure API Management till en fil i ett av de format som stöds.</span><span class="sxs-lookup"><span data-stu-id="73934-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="73934-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73934-109">EXAMPLES</span></span>

### <span data-ttu-id="73934-110">Exempel 1: exportera ett API i WADL-format (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="73934-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="73934-111">Det här kommandot exporterar ett API till en WADL-fil.</span><span class="sxs-lookup"><span data-stu-id="73934-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="73934-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73934-112">PARAMETERS</span></span>

### <span data-ttu-id="73934-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="73934-113">-ApiId</span></span>
<span data-ttu-id="73934-114">Anger ID för det API som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="73934-114">Specifies the ID of the API to export.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73934-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="73934-115">-Context</span></span>
<span data-ttu-id="73934-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="73934-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73934-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73934-117">-DefaultProfile</span></span>
<span data-ttu-id="73934-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73934-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73934-119">-Force</span><span class="sxs-lookup"><span data-stu-id="73934-119">-Force</span></span>
<span data-ttu-id="73934-120">Anger att den här åtgärden ersätter filen med samma namn om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="73934-120">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73934-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73934-121">-PassThru</span></span>
<span data-ttu-id="73934-122">Anger att den här åtgärden returnerar $True om API: t exporteras eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="73934-122">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73934-123">-Spara som</span><span class="sxs-lookup"><span data-stu-id="73934-123">-SaveAs</span></span>
<span data-ttu-id="73934-124">Anger sökvägen till den plats där du vill spara det exporterade API: t.</span><span class="sxs-lookup"><span data-stu-id="73934-124">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73934-125">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="73934-125">-SpecificationFormat</span></span>
<span data-ttu-id="73934-126">Anger API-formatet.</span><span class="sxs-lookup"><span data-stu-id="73934-126">Specifies the API format.</span></span>
<span data-ttu-id="73934-127">psdx_paramvalues Wadl och swagger.</span><span class="sxs-lookup"><span data-stu-id="73934-127">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73934-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73934-128">-Confirm</span></span>
<span data-ttu-id="73934-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73934-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73934-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73934-130">-WhatIf</span></span>
<span data-ttu-id="73934-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73934-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73934-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73934-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73934-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73934-133">CommonParameters</span></span>
<span data-ttu-id="73934-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73934-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73934-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73934-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73934-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73934-136">INPUTS</span></span>

### <span data-ttu-id="73934-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="73934-137">None</span></span>
<span data-ttu-id="73934-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="73934-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73934-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73934-139">OUTPUTS</span></span>

### <span data-ttu-id="73934-140">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="73934-140">String</span></span>
<span data-ttu-id="73934-141">Denna cmdlet returnerar det exporterade API-innehållet som en sträng.</span><span class="sxs-lookup"><span data-stu-id="73934-141">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="73934-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73934-142">NOTES</span></span>

## <span data-ttu-id="73934-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73934-143">RELATED LINKS</span></span>

[<span data-ttu-id="73934-144">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="73934-144">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="73934-145">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="73934-145">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="73934-146">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="73934-146">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="73934-147">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="73934-147">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="73934-148">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="73934-148">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


