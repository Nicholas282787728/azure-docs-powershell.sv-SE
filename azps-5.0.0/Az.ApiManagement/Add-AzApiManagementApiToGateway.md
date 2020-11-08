---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271122"
---
# <span data-ttu-id="e9d2e-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="e9d2e-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="e9d2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d2e-103">Bifogar ett API till en gateway.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="e9d2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9d2e-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9d2e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d2e-106">Cmdleten **Add-AzApiManagementApiToGateway** lägger till en API för Azure API Management till en gateway.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="e9d2e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9d2e-107">EXAMPLES</span></span>

### <span data-ttu-id="e9d2e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9d2e-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="e9d2e-109">Det här kommandot lägger till angivet API till angiven Gateway.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="e9d2e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9d2e-110">PARAMETERS</span></span>

### <span data-ttu-id="e9d2e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e9d2e-111">-ApiId</span></span>
<span data-ttu-id="e9d2e-112">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-112">Identifier of existing API.</span></span>
<span data-ttu-id="e9d2e-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e9d2e-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e9d2e-114">-Context</span></span>
<span data-ttu-id="e9d2e-115">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e9d2e-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="e9d2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d2e-117">-DefaultProfile</span></span>
<span data-ttu-id="e9d2e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9d2e-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e9d2e-119">-GatewayId</span></span>
<span data-ttu-id="e9d2e-120">Identifierare för befintlig gateway.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="e9d2e-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e9d2e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9d2e-122">-PassThru</span></span>
<span data-ttu-id="e9d2e-123">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e9d2e-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-124">This parameter is optional.</span></span>
<span data-ttu-id="e9d2e-125">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-125">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d2e-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="e9d2e-126">-ProvisioningState</span></span>
<span data-ttu-id="e9d2e-127">Etablerings status (skapad).</span><span class="sxs-lookup"><span data-stu-id="e9d2e-127">Provisioning State (Created).</span></span>
<span data-ttu-id="e9d2e-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d2e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9d2e-129">-Confirm</span></span>
<span data-ttu-id="e9d2e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9d2e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9d2e-131">-WhatIf</span></span>
<span data-ttu-id="e9d2e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9d2e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9d2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d2e-134">CommonParameters</span></span>
<span data-ttu-id="e9d2e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d2e-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9d2e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d2e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9d2e-137">INPUTS</span></span>

### <span data-ttu-id="e9d2e-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9d2e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9d2e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e9d2e-139">System.String</span></span>

### <span data-ttu-id="e9d2e-140">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayApiProvisioningState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 2.0.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e9d2e-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e9d2e-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e9d2e-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e9d2e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9d2e-142">OUTPUTS</span></span>

### <span data-ttu-id="e9d2e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9d2e-143">System.Boolean</span></span>

## <span data-ttu-id="e9d2e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9d2e-144">NOTES</span></span>

## <span data-ttu-id="e9d2e-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9d2e-145">RELATED LINKS</span></span>

[<span data-ttu-id="e9d2e-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="e9d2e-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)