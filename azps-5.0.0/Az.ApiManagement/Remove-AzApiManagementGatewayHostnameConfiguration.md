---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271382"
---
# <span data-ttu-id="e42b0-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e42b0-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="e42b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e42b0-102">SYNOPSIS</span></span>
<span data-ttu-id="e42b0-103">Tar bort en värd konfiguration från den befintliga gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e42b0-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="e42b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e42b0-104">SYNTAX</span></span>

### <span data-ttu-id="e42b0-105">ContextParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="e42b0-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e42b0-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42b0-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e42b0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42b0-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e42b0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e42b0-108">DESCRIPTION</span></span>
<span data-ttu-id="e42b0-109">Cmdleten **Remove-AzApiManagementGatewayHostnameConfiguration** tar bort en värd konfiguration från den befintliga gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e42b0-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="e42b0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e42b0-110">EXAMPLES</span></span>

### <span data-ttu-id="e42b0-111">Exempel 1: ta bort en befintlig gateway hostname-konfiguration</span><span class="sxs-lookup"><span data-stu-id="e42b0-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="e42b0-112">Med det här kommandot tas en befintlig gateway-konfiguration bort och användaren uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e42b0-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="e42b0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e42b0-113">PARAMETERS</span></span>

### <span data-ttu-id="e42b0-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e42b0-114">-Context</span></span>
<span data-ttu-id="e42b0-115">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e42b0-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e42b0-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e42b0-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e42b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42b0-117">-DefaultProfile</span></span>
<span data-ttu-id="e42b0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e42b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e42b0-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e42b0-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="e42b0-120">Identifierare för befintlig gateway-värdnamn-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e42b0-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="e42b0-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e42b0-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42b0-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e42b0-122">-GatewayId</span></span>
<span data-ttu-id="e42b0-123">Identifierare för befintlig gateway.</span><span class="sxs-lookup"><span data-stu-id="e42b0-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="e42b0-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e42b0-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42b0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e42b0-125">-InputObject</span></span>
<span data-ttu-id="e42b0-126">Instans av PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e42b0-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="e42b0-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e42b0-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e42b0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e42b0-128">-PassThru</span></span>
<span data-ttu-id="e42b0-129">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="e42b0-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e42b0-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e42b0-130">This parameter is optional.</span></span>
<span data-ttu-id="e42b0-131">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="e42b0-131">Default value is false.</span></span>

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

### <span data-ttu-id="e42b0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e42b0-132">-ResourceId</span></span>
<span data-ttu-id="e42b0-133">GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e42b0-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="e42b0-134">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e42b0-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42b0-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e42b0-135">-Confirm</span></span>
<span data-ttu-id="e42b0-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e42b0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e42b0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e42b0-137">-WhatIf</span></span>
<span data-ttu-id="e42b0-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e42b0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e42b0-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e42b0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e42b0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42b0-140">CommonParameters</span></span>
<span data-ttu-id="e42b0-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42b0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42b0-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e42b0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42b0-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e42b0-143">INPUTS</span></span>

### <span data-ttu-id="e42b0-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e42b0-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e42b0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e42b0-145">System.String</span></span>

### <span data-ttu-id="e42b0-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e42b0-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e42b0-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e42b0-147">OUTPUTS</span></span>

### <span data-ttu-id="e42b0-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e42b0-148">System.Boolean</span></span>

## <span data-ttu-id="e42b0-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e42b0-149">NOTES</span></span>

## <span data-ttu-id="e42b0-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e42b0-150">RELATED LINKS</span></span>
