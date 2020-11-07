---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 7dc06f280595551a9e054c251339e96163b798b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756041"
---
# <span data-ttu-id="ea8de-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ea8de-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="ea8de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea8de-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8de-103">Exporterar ett API till en fil.</span><span class="sxs-lookup"><span data-stu-id="ea8de-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea8de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea8de-104">SYNTAX</span></span>

### <span data-ttu-id="ea8de-105">ExportToPipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="ea8de-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8de-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="ea8de-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8de-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea8de-107">DESCRIPTION</span></span>
<span data-ttu-id="ea8de-108">Cmdleten **export-AzureRmApiManagementApi** exporterar ett API för Azure API Management till en fil i ett av de format som stöds.</span><span class="sxs-lookup"><span data-stu-id="ea8de-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="ea8de-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea8de-109">EXAMPLES</span></span>

### <span data-ttu-id="ea8de-110">Exempel 1: exportera ett API i WADL-format (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="ea8de-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="ea8de-111">Det här kommandot exporterar ett API till en WADL-fil.</span><span class="sxs-lookup"><span data-stu-id="ea8de-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="ea8de-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea8de-112">PARAMETERS</span></span>

### <span data-ttu-id="ea8de-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ea8de-113">-ApiId</span></span>
<span data-ttu-id="ea8de-114">Anger ID för det API som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="ea8de-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="ea8de-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ea8de-115">-ApiRevision</span></span>
<span data-ttu-id="ea8de-116">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="ea8de-116">Identifier of API Revision.</span></span> <span data-ttu-id="ea8de-117">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ea8de-117">This parameter is optional.</span></span> <span data-ttu-id="ea8de-118">Om du inte anger det här alternativet görs exporten för den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="ea8de-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="ea8de-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ea8de-119">-Context</span></span>
<span data-ttu-id="ea8de-120">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ea8de-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ea8de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8de-121">-DefaultProfile</span></span>
<span data-ttu-id="ea8de-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8de-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea8de-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ea8de-123">-Force</span></span>
<span data-ttu-id="ea8de-124">Anger att den här åtgärden ersätter filen med samma namn om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="ea8de-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="ea8de-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea8de-125">-PassThru</span></span>
<span data-ttu-id="ea8de-126">Anger att den här åtgärden returnerar $True om API: t exporteras eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="ea8de-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="ea8de-127">-Spara som</span><span class="sxs-lookup"><span data-stu-id="ea8de-127">-SaveAs</span></span>
<span data-ttu-id="ea8de-128">Anger sökvägen till den plats där du vill spara det exporterade API: t.</span><span class="sxs-lookup"><span data-stu-id="ea8de-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="ea8de-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="ea8de-129">-SpecificationFormat</span></span>
<span data-ttu-id="ea8de-130">Anger API-formatet.</span><span class="sxs-lookup"><span data-stu-id="ea8de-130">Specifies the API format.</span></span>
<span data-ttu-id="ea8de-131">psdx_paramvalues Wadl och swagger.</span><span class="sxs-lookup"><span data-stu-id="ea8de-131">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="ea8de-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea8de-132">-Confirm</span></span>
<span data-ttu-id="ea8de-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea8de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8de-134">-WhatIf</span></span>
<span data-ttu-id="ea8de-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea8de-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8de-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea8de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8de-137">CommonParameters</span></span>
<span data-ttu-id="ea8de-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8de-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8de-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8de-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea8de-140">INPUTS</span></span>

### <span data-ttu-id="ea8de-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ea8de-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ea8de-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ea8de-142">System.String</span></span>

### <span data-ttu-id="ea8de-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="ea8de-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="ea8de-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ea8de-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ea8de-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea8de-145">OUTPUTS</span></span>

### <span data-ttu-id="ea8de-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ea8de-146">System.String</span></span>
<span data-ttu-id="ea8de-147">Denna cmdlet returnerar det exporterade API-innehållet som en sträng.</span><span class="sxs-lookup"><span data-stu-id="ea8de-147">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="ea8de-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea8de-148">NOTES</span></span>

## <span data-ttu-id="ea8de-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea8de-149">RELATED LINKS</span></span>

[<span data-ttu-id="ea8de-150">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ea8de-150">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="ea8de-151">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ea8de-151">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="ea8de-152">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ea8de-152">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="ea8de-153">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ea8de-153">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="ea8de-154">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ea8de-154">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


