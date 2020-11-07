---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755224"
---
# <span data-ttu-id="527d4-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="527d4-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="527d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="527d4-102">SYNOPSIS</span></span>
<span data-ttu-id="527d4-103">Tar bort en viss API-version</span><span class="sxs-lookup"><span data-stu-id="527d4-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="527d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="527d4-104">SYNTAX</span></span>

### <span data-ttu-id="527d4-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="527d4-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="527d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="527d4-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="527d4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="527d4-107">DESCRIPTION</span></span>

<span data-ttu-id="527d4-108">Cmdleten **Remove-AzureRmApiManagementApiVersionSet** tar bort en befintlig API-version.</span><span class="sxs-lookup"><span data-stu-id="527d4-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="527d4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="527d4-109">EXAMPLES</span></span>

### <span data-ttu-id="527d4-110">Exempel 1: ta bort en API-version</span><span class="sxs-lookup"><span data-stu-id="527d4-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="527d4-111">Det här kommandot tar bort API-versionen med angiven ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="527d4-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="527d4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="527d4-112">PARAMETERS</span></span>

### <span data-ttu-id="527d4-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="527d4-113">-ApiVersionSetId</span></span>
<span data-ttu-id="527d4-114">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="527d4-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="527d4-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="527d4-115">This parameter is required.</span></span>

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

### <span data-ttu-id="527d4-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="527d4-116">-Context</span></span>
<span data-ttu-id="527d4-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="527d4-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="527d4-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="527d4-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="527d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="527d4-119">-DefaultProfile</span></span>
<span data-ttu-id="527d4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="527d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="527d4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="527d4-121">-InputObject</span></span>
<span data-ttu-id="527d4-122">Instans av PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="527d4-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="527d4-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="527d4-123">This parameter is required.</span></span>

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

### <span data-ttu-id="527d4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="527d4-124">-PassThru</span></span>
<span data-ttu-id="527d4-125">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="527d4-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="527d4-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="527d4-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="527d4-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="527d4-127">-Confirm</span></span>
<span data-ttu-id="527d4-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="527d4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="527d4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="527d4-129">-WhatIf</span></span>
<span data-ttu-id="527d4-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="527d4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="527d4-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="527d4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="527d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527d4-132">CommonParameters</span></span>
<span data-ttu-id="527d4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="527d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527d4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="527d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527d4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="527d4-135">INPUTS</span></span>

### <span data-ttu-id="527d4-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="527d4-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="527d4-137">Parametrar: kontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="527d4-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="527d4-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="527d4-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="527d4-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="527d4-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="527d4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="527d4-140">System.String</span></span>

## <span data-ttu-id="527d4-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="527d4-141">OUTPUTS</span></span>

### <span data-ttu-id="527d4-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="527d4-142">System.Boolean</span></span>

## <span data-ttu-id="527d4-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="527d4-143">NOTES</span></span>

## <span data-ttu-id="527d4-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="527d4-144">RELATED LINKS</span></span>

[<span data-ttu-id="527d4-145">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="527d4-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="527d4-146">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="527d4-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="527d4-147">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="527d4-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
