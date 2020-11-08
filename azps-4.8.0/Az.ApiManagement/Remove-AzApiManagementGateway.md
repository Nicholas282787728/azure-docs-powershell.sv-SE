---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101780"
---
# <span data-ttu-id="08fb6-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="08fb6-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="08fb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="08fb6-103">Tar bort ett API från en gateway.</span><span class="sxs-lookup"><span data-stu-id="08fb6-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="08fb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08fb6-104">SYNTAX</span></span>

### <span data-ttu-id="08fb6-105">ContextParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="08fb6-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08fb6-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08fb6-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08fb6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08fb6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08fb6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08fb6-108">DESCRIPTION</span></span>
<span data-ttu-id="08fb6-109">Cmdleten **Remove-AzApiManagementGateway kopplar bort** ett API från en gateway.</span><span class="sxs-lookup"><span data-stu-id="08fb6-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="08fb6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08fb6-110">EXAMPLES</span></span>

### <span data-ttu-id="08fb6-111">Exempel 1: ta bort en befintlig gateway</span><span class="sxs-lookup"><span data-stu-id="08fb6-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="08fb6-112">Detta kommando tar bort en befintlig gateway och ber inte användaren att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="08fb6-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="08fb6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08fb6-113">PARAMETERS</span></span>

### <span data-ttu-id="08fb6-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="08fb6-114">-Context</span></span>
<span data-ttu-id="08fb6-115">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="08fb6-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="08fb6-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="08fb6-116">This parameter is required.</span></span>

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

### <span data-ttu-id="08fb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08fb6-117">-DefaultProfile</span></span>
<span data-ttu-id="08fb6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08fb6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08fb6-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="08fb6-119">-GatewayId</span></span>
<span data-ttu-id="08fb6-120">Identifierare för befintlig gateway.</span><span class="sxs-lookup"><span data-stu-id="08fb6-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="08fb6-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="08fb6-121">This parameter is required.</span></span>

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

### <span data-ttu-id="08fb6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08fb6-122">-InputObject</span></span>
<span data-ttu-id="08fb6-123">Instans av PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="08fb6-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="08fb6-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="08fb6-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08fb6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08fb6-125">-PassThru</span></span>
<span data-ttu-id="08fb6-126">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="08fb6-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="08fb6-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="08fb6-127">This parameter is optional.</span></span>
<span data-ttu-id="08fb6-128">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="08fb6-128">Default value is false.</span></span>

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

### <span data-ttu-id="08fb6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08fb6-129">-ResourceId</span></span>
<span data-ttu-id="08fb6-130">Gatewayens arm-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="08fb6-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="08fb6-131">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="08fb6-131">This parameter is required.</span></span>

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

### <span data-ttu-id="08fb6-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08fb6-132">-Confirm</span></span>
<span data-ttu-id="08fb6-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08fb6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08fb6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08fb6-134">-WhatIf</span></span>
<span data-ttu-id="08fb6-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08fb6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08fb6-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08fb6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08fb6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08fb6-137">CommonParameters</span></span>
<span data-ttu-id="08fb6-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08fb6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08fb6-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08fb6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08fb6-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08fb6-140">INPUTS</span></span>

### <span data-ttu-id="08fb6-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="08fb6-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="08fb6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="08fb6-142">System.String</span></span>

### <span data-ttu-id="08fb6-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08fb6-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="08fb6-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08fb6-144">OUTPUTS</span></span>

### <span data-ttu-id="08fb6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08fb6-145">System.Boolean</span></span>

## <span data-ttu-id="08fb6-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08fb6-146">NOTES</span></span>

## <span data-ttu-id="08fb6-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08fb6-147">RELATED LINKS</span></span>
