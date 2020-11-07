---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 1c322669431377b96f0bc45e1228c52ba70c6d68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743429"
---
# <span data-ttu-id="79233-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79233-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="79233-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79233-102">SYNOPSIS</span></span>
<span data-ttu-id="79233-103">Exporterar ett API till en fil.</span><span class="sxs-lookup"><span data-stu-id="79233-103">Exports an API to a file.</span></span>

## <span data-ttu-id="79233-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79233-104">SYNTAX</span></span>

### <span data-ttu-id="79233-105">ExportToPipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="79233-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79233-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="79233-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79233-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79233-107">DESCRIPTION</span></span>
<span data-ttu-id="79233-108">Cmdleten **export-AzApiManagementApi** exporterar ett API för Azure API Management till en fil i ett av de format som stöds.</span><span class="sxs-lookup"><span data-stu-id="79233-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="79233-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79233-109">EXAMPLES</span></span>

### <span data-ttu-id="79233-110">Exempel 1: exportera ett API i WADL-format (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="79233-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="79233-111">Det här kommandot exporterar ett API till en WADL-fil.</span><span class="sxs-lookup"><span data-stu-id="79233-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="79233-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79233-112">PARAMETERS</span></span>

### <span data-ttu-id="79233-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="79233-113">-ApiId</span></span>
<span data-ttu-id="79233-114">Anger ID för det API som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="79233-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="79233-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="79233-115">-ApiRevision</span></span>
<span data-ttu-id="79233-116">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="79233-116">Identifier of API Revision.</span></span> <span data-ttu-id="79233-117">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="79233-117">This parameter is optional.</span></span> <span data-ttu-id="79233-118">Om du inte anger det här alternativet görs exporten för den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="79233-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="79233-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="79233-119">-Context</span></span>
<span data-ttu-id="79233-120">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79233-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="79233-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79233-121">-DefaultProfile</span></span>
<span data-ttu-id="79233-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79233-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79233-123">-Force</span><span class="sxs-lookup"><span data-stu-id="79233-123">-Force</span></span>
<span data-ttu-id="79233-124">Anger att den här åtgärden ersätter filen med samma namn om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="79233-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="79233-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79233-125">-PassThru</span></span>
<span data-ttu-id="79233-126">Anger att den här åtgärden returnerar $True om API: t exporteras eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="79233-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="79233-127">-Spara som</span><span class="sxs-lookup"><span data-stu-id="79233-127">-SaveAs</span></span>
<span data-ttu-id="79233-128">Anger sökvägen till den plats där du vill spara det exporterade API: t.</span><span class="sxs-lookup"><span data-stu-id="79233-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="79233-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="79233-129">-SpecificationFormat</span></span>
<span data-ttu-id="79233-130">Anger API-formatet.</span><span class="sxs-lookup"><span data-stu-id="79233-130">Specifies the API format.</span></span>
<span data-ttu-id="79233-131">psdx_paramvalues Wadl och swagger.</span><span class="sxs-lookup"><span data-stu-id="79233-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79233-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79233-132">-Confirm</span></span>
<span data-ttu-id="79233-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79233-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79233-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79233-134">-WhatIf</span></span>
<span data-ttu-id="79233-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79233-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79233-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79233-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79233-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79233-137">CommonParameters</span></span>
<span data-ttu-id="79233-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79233-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79233-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79233-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79233-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79233-140">INPUTS</span></span>

### <span data-ttu-id="79233-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79233-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79233-142">System. String</span><span class="sxs-lookup"><span data-stu-id="79233-142">System.String</span></span>

### <span data-ttu-id="79233-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="79233-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="79233-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79233-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79233-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79233-145">OUTPUTS</span></span>

### <span data-ttu-id="79233-146">System. String</span><span class="sxs-lookup"><span data-stu-id="79233-146">System.String</span></span>

## <span data-ttu-id="79233-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79233-147">NOTES</span></span>

## <span data-ttu-id="79233-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79233-148">RELATED LINKS</span></span>

[<span data-ttu-id="79233-149">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79233-149">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="79233-150">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79233-150">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="79233-151">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79233-151">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="79233-152">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79233-152">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="79233-153">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79233-153">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


