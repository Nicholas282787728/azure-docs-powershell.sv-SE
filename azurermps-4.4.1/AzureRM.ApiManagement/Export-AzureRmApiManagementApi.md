---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 09400d3111ffb3fda232e1cbb71fd0aac063a74c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756644"
---
# <span data-ttu-id="6fd70-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6fd70-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="6fd70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fd70-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd70-103">Exporterar ett API till en fil.</span><span class="sxs-lookup"><span data-stu-id="6fd70-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fd70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fd70-104">SYNTAX</span></span>

### <span data-ttu-id="6fd70-105">Exportera till pipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="6fd70-105">Export to pipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd70-106">Exportera till fil</span><span class="sxs-lookup"><span data-stu-id="6fd70-106">Export to File</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd70-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fd70-107">DESCRIPTION</span></span>
<span data-ttu-id="6fd70-108">Cmdleten **export-AzureRmApiManagementApi** exporterar ett API för Azure API Management till en fil i ett av de format som stöds.</span><span class="sxs-lookup"><span data-stu-id="6fd70-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="6fd70-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fd70-109">EXAMPLES</span></span>

### <span data-ttu-id="6fd70-110">Exempel 1: exportera ett API i WADL-format (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="6fd70-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="6fd70-111">Det här kommandot exporterar ett API till en WADL-fil.</span><span class="sxs-lookup"><span data-stu-id="6fd70-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="6fd70-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fd70-112">PARAMETERS</span></span>

### <span data-ttu-id="6fd70-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6fd70-113">-ApiId</span></span>
<span data-ttu-id="6fd70-114">Anger ID för det API som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="6fd70-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="6fd70-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6fd70-115">-Context</span></span>
<span data-ttu-id="6fd70-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6fd70-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6fd70-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6fd70-117">-Force</span></span>
<span data-ttu-id="6fd70-118">Anger att den här åtgärden ersätter filen med samma namn om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="6fd70-118">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd70-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fd70-119">-PassThru</span></span>
<span data-ttu-id="6fd70-120">Anger att den här åtgärden returnerar $True om API: t exporteras eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="6fd70-120">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd70-121">-Spara som</span><span class="sxs-lookup"><span data-stu-id="6fd70-121">-SaveAs</span></span>
<span data-ttu-id="6fd70-122">Anger sökvägen till den plats där du vill spara det exporterade API: t.</span><span class="sxs-lookup"><span data-stu-id="6fd70-122">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd70-123">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="6fd70-123">-SpecificationFormat</span></span>
<span data-ttu-id="6fd70-124">Anger API-formatet.</span><span class="sxs-lookup"><span data-stu-id="6fd70-124">Specifies the API format.</span></span>
<span data-ttu-id="6fd70-125">psdx_paramvalues Wadl och swagger.</span><span class="sxs-lookup"><span data-stu-id="6fd70-125">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="6fd70-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6fd70-126">-Confirm</span></span>
<span data-ttu-id="6fd70-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6fd70-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd70-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd70-128">-WhatIf</span></span>
<span data-ttu-id="6fd70-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6fd70-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd70-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6fd70-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd70-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd70-131">-DefaultProfile</span></span>
<span data-ttu-id="6fd70-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd70-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fd70-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd70-133">CommonParameters</span></span>
<span data-ttu-id="6fd70-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd70-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd70-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd70-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd70-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fd70-136">INPUTS</span></span>

## <span data-ttu-id="6fd70-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fd70-137">OUTPUTS</span></span>

### <span data-ttu-id="6fd70-138">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="6fd70-138">String</span></span>
<span data-ttu-id="6fd70-139">Denna cmdlet returnerar det exporterade API-innehållet som en sträng.</span><span class="sxs-lookup"><span data-stu-id="6fd70-139">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="6fd70-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fd70-140">NOTES</span></span>

## <span data-ttu-id="6fd70-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fd70-141">RELATED LINKS</span></span>

[<span data-ttu-id="6fd70-142">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6fd70-142">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="6fd70-143">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6fd70-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="6fd70-144">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6fd70-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="6fd70-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6fd70-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="6fd70-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6fd70-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


