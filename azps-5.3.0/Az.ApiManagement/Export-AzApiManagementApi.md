---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525136"
---
# <span data-ttu-id="4608c-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4608c-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="4608c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4608c-102">SYNOPSIS</span></span>
<span data-ttu-id="4608c-103">Exporterar ett API till en fil.</span><span class="sxs-lookup"><span data-stu-id="4608c-103">Exports an API to a file.</span></span>

## <span data-ttu-id="4608c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4608c-104">SYNTAX</span></span>

### <span data-ttu-id="4608c-105">ExportToPipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="4608c-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4608c-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="4608c-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4608c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4608c-107">DESCRIPTION</span></span>
<span data-ttu-id="4608c-108">Cmdleten **export-AzApiManagementApi** exporterar ett API för Azure API Management till en fil i ett av de format som stöds.</span><span class="sxs-lookup"><span data-stu-id="4608c-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="4608c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4608c-109">EXAMPLES</span></span>

### <span data-ttu-id="4608c-110">Exempel 1: exportera ett API i WADL-format (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="4608c-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="4608c-111">Det här kommandot exporterar ett API till en WADL-fil.</span><span class="sxs-lookup"><span data-stu-id="4608c-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="4608c-112">Exempel 2: exportera ett API i OpenApi 3,0 Specifikations format som JSON-dokument</span><span class="sxs-lookup"><span data-stu-id="4608c-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="4608c-113">Det här kommandot exporterar en API-definitioner i Open API format som JSON-dokument</span><span class="sxs-lookup"><span data-stu-id="4608c-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="4608c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4608c-114">PARAMETERS</span></span>

### <span data-ttu-id="4608c-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4608c-115">-ApiId</span></span>
<span data-ttu-id="4608c-116">Anger ID för det API som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="4608c-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="4608c-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4608c-117">-ApiRevision</span></span>
<span data-ttu-id="4608c-118">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="4608c-118">Identifier of API Revision.</span></span> <span data-ttu-id="4608c-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="4608c-119">This parameter is optional.</span></span> <span data-ttu-id="4608c-120">Om du inte anger det här alternativet görs exporten för den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="4608c-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="4608c-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4608c-121">-Context</span></span>
<span data-ttu-id="4608c-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4608c-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4608c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4608c-123">-DefaultProfile</span></span>
<span data-ttu-id="4608c-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4608c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4608c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4608c-125">-Force</span></span>
<span data-ttu-id="4608c-126">Anger att den här åtgärden ersätter filen med samma namn om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="4608c-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4608c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4608c-127">-PassThru</span></span>
<span data-ttu-id="4608c-128">Anger att den här åtgärden returnerar $True om API: t exporteras eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="4608c-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4608c-129">-Spara som</span><span class="sxs-lookup"><span data-stu-id="4608c-129">-SaveAs</span></span>
<span data-ttu-id="4608c-130">Anger sökvägen till den plats där du vill spara det exporterade API: t.</span><span class="sxs-lookup"><span data-stu-id="4608c-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4608c-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="4608c-131">-SpecificationFormat</span></span>
<span data-ttu-id="4608c-132">Anger API-formatet.</span><span class="sxs-lookup"><span data-stu-id="4608c-132">Specifies the API format.</span></span>
<span data-ttu-id="4608c-133">psdx_paramvalues Wadl, WSDL, Swagger, OpenApi och OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="4608c-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4608c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4608c-134">-Confirm</span></span>
<span data-ttu-id="4608c-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4608c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4608c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4608c-136">-WhatIf</span></span>
<span data-ttu-id="4608c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4608c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4608c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4608c-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4608c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4608c-139">CommonParameters</span></span>
<span data-ttu-id="4608c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4608c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4608c-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4608c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4608c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4608c-142">INPUTS</span></span>

### <span data-ttu-id="4608c-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4608c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4608c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4608c-144">System.String</span></span>

### <span data-ttu-id="4608c-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="4608c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="4608c-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4608c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4608c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4608c-147">OUTPUTS</span></span>

### <span data-ttu-id="4608c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4608c-148">System.String</span></span>

## <span data-ttu-id="4608c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4608c-149">NOTES</span></span>

## <span data-ttu-id="4608c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4608c-150">RELATED LINKS</span></span>

[<span data-ttu-id="4608c-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4608c-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="4608c-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4608c-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="4608c-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4608c-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="4608c-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4608c-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="4608c-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4608c-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


