---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917802"
---
# <span data-ttu-id="2d871-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d871-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="2d871-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d871-102">SYNOPSIS</span></span>
<span data-ttu-id="2d871-103">Tar bort en viss API-version</span><span class="sxs-lookup"><span data-stu-id="2d871-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="2d871-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d871-104">SYNTAX</span></span>

### <span data-ttu-id="2d871-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="2d871-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d871-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2d871-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d871-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d871-107">DESCRIPTION</span></span>

<span data-ttu-id="2d871-108">Cmdleten **Remove-AzAzureRmApiManagementApiVersionSet** tar bort en befintlig API-version.</span><span class="sxs-lookup"><span data-stu-id="2d871-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="2d871-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d871-109">EXAMPLES</span></span>

### <span data-ttu-id="2d871-110">Exempel 1: ta bort en API-version</span><span class="sxs-lookup"><span data-stu-id="2d871-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="2d871-111">Det här kommandot tar bort API-versionen med angiven ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="2d871-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="2d871-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d871-112">PARAMETERS</span></span>

### <span data-ttu-id="2d871-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="2d871-113">-ApiVersionSetId</span></span>
<span data-ttu-id="2d871-114">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="2d871-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="2d871-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2d871-115">This parameter is required.</span></span>

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

### <span data-ttu-id="2d871-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2d871-116">-Context</span></span>
<span data-ttu-id="2d871-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2d871-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2d871-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2d871-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2d871-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d871-119">-DefaultProfile</span></span>
<span data-ttu-id="2d871-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d871-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d871-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d871-121">-InputObject</span></span>
<span data-ttu-id="2d871-122">Instans av PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2d871-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="2d871-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2d871-123">This parameter is required.</span></span>

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

### <span data-ttu-id="2d871-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d871-124">-PassThru</span></span>
<span data-ttu-id="2d871-125">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="2d871-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2d871-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2d871-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="2d871-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d871-127">-Confirm</span></span>
<span data-ttu-id="2d871-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d871-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d871-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d871-129">-WhatIf</span></span>
<span data-ttu-id="2d871-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d871-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d871-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d871-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d871-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d871-132">CommonParameters</span></span>
<span data-ttu-id="2d871-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d871-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d871-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d871-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d871-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d871-135">INPUTS</span></span>

### <span data-ttu-id="2d871-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2d871-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2d871-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d871-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="2d871-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2d871-138">System.String</span></span>

## <span data-ttu-id="2d871-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d871-139">OUTPUTS</span></span>

### <span data-ttu-id="2d871-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d871-140">System.Boolean</span></span>

## <span data-ttu-id="2d871-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d871-141">NOTES</span></span>

## <span data-ttu-id="2d871-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d871-142">RELATED LINKS</span></span>

[<span data-ttu-id="2d871-143">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d871-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="2d871-144">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d871-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="2d871-145">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d871-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)