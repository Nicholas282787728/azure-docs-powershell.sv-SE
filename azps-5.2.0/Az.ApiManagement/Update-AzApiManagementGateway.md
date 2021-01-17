---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408091"
---
# <span data-ttu-id="6ad67-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6ad67-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="6ad67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ad67-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad67-103">Konfigurerar en API-hanterings-Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ad67-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="6ad67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ad67-104">SYNTAX</span></span>

### <span data-ttu-id="6ad67-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="6ad67-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad67-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6ad67-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad67-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad67-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad67-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ad67-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad67-109">Cmdleten **Update-AzApiManagementGateway** konfigurerar en API Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ad67-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="6ad67-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ad67-110">EXAMPLES</span></span>

### <span data-ttu-id="6ad67-111">Exempel 1: Konfigurera en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="6ad67-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="6ad67-112">Det här kommandot konfigurerar en gateway.</span><span class="sxs-lookup"><span data-stu-id="6ad67-112">This command configures a gateway.</span></span>

## <span data-ttu-id="6ad67-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ad67-113">PARAMETERS</span></span>

### <span data-ttu-id="6ad67-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6ad67-114">-Context</span></span>
<span data-ttu-id="6ad67-115">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6ad67-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6ad67-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6ad67-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad67-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad67-117">-DefaultProfile</span></span>
<span data-ttu-id="6ad67-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad67-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad67-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6ad67-119">-Description</span></span>
<span data-ttu-id="6ad67-120">Beskrivning av gatewayen.</span><span class="sxs-lookup"><span data-stu-id="6ad67-120">Gateway description.</span></span>
<span data-ttu-id="6ad67-121">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="6ad67-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="6ad67-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="6ad67-122">-GatewayId</span></span>
<span data-ttu-id="6ad67-123">Identifierare för befintlig gateway.</span><span class="sxs-lookup"><span data-stu-id="6ad67-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="6ad67-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6ad67-124">This parameter is required.</span></span>

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

### <span data-ttu-id="6ad67-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ad67-125">-InputObject</span></span>
<span data-ttu-id="6ad67-126">Instans av PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="6ad67-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="6ad67-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6ad67-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad67-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="6ad67-128">-LocationData</span></span>
<span data-ttu-id="6ad67-129">Gateway-plats.</span><span class="sxs-lookup"><span data-stu-id="6ad67-129">Gateway location.</span></span>
<span data-ttu-id="6ad67-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="6ad67-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad67-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ad67-131">-PassThru</span></span>
<span data-ttu-id="6ad67-132">Om det anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway typ som representerar den modifierade gatewayen.</span><span class="sxs-lookup"><span data-stu-id="6ad67-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="6ad67-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad67-133">-ResourceId</span></span>
<span data-ttu-id="6ad67-134">Gatewayens arm-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6ad67-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="6ad67-135">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6ad67-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad67-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ad67-136">-Confirm</span></span>
<span data-ttu-id="6ad67-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6ad67-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad67-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad67-138">-WhatIf</span></span>
<span data-ttu-id="6ad67-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ad67-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad67-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ad67-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad67-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad67-141">CommonParameters</span></span>
<span data-ttu-id="6ad67-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad67-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad67-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ad67-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad67-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ad67-144">INPUTS</span></span>

### <span data-ttu-id="6ad67-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6ad67-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6ad67-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad67-146">System.String</span></span>

### <span data-ttu-id="6ad67-147">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="6ad67-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="6ad67-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ad67-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6ad67-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ad67-149">OUTPUTS</span></span>

### <span data-ttu-id="6ad67-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6ad67-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="6ad67-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ad67-151">NOTES</span></span>

## <span data-ttu-id="6ad67-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ad67-152">RELATED LINKS</span></span>
