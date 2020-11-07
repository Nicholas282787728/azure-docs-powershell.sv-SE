---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 2daec87c79e02d6aa4d2720bb20cac5194d1a752
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747025"
---
# <span data-ttu-id="5d370-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d370-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="5d370-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d370-102">SYNOPSIS</span></span>
<span data-ttu-id="5d370-103">Avbryter en resurs grupps distribution.</span><span class="sxs-lookup"><span data-stu-id="5d370-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="5d370-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d370-104">SYNTAX</span></span>

### <span data-ttu-id="5d370-105">StopByResourceGroupDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="5d370-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d370-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5d370-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d370-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d370-107">DESCRIPTION</span></span>
<span data-ttu-id="5d370-108">Cmdleten **Stop-AzResourceGroupDeployment** avbryter en Azure Resource Group-distribution som har startat men inte slutförts.</span><span class="sxs-lookup"><span data-stu-id="5d370-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="5d370-109">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="5d370-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="5d370-110">En Azure-resurs är en användardefinierad enhet, till exempel en webbplats, databas eller databas server.</span><span class="sxs-lookup"><span data-stu-id="5d370-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="5d370-111">En resurs grupp är en samling resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="5d370-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="5d370-112">Använd New-AzResourceGroupDeployment cmdlet för att distribuera en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5d370-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="5d370-113">New-AzResource-cmdleten skapar en ny resurs men den utlöser inte en distributions åtgärd för en resurs grupp som denna cmdlet kan stoppa.</span><span class="sxs-lookup"><span data-stu-id="5d370-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="5d370-114">Denna cmdlet stoppar bara en drift sättning.</span><span class="sxs-lookup"><span data-stu-id="5d370-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="5d370-115">Använd parametern *namn* för att stoppa en specifik distribution.</span><span class="sxs-lookup"><span data-stu-id="5d370-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="5d370-116">Om du utelämnar parametern *Name* söker **Stop-AzResourceGroupDeployment** efter en pågående installation och stoppar den.</span><span class="sxs-lookup"><span data-stu-id="5d370-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="5d370-117">Om en cmdlet hittar mer än en drifts distribution Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="5d370-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="5d370-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d370-118">EXAMPLES</span></span>

### <span data-ttu-id="5d370-119">Exempel 1: starta och stoppa en distribution av en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="5d370-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="5d370-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d370-120">PARAMETERS</span></span>

### <span data-ttu-id="5d370-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5d370-121">-ApiVersion</span></span>
<span data-ttu-id="5d370-122">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="5d370-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5d370-123">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="5d370-123">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d370-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d370-124">-DefaultProfile</span></span>
<span data-ttu-id="5d370-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5d370-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d370-126">-ID</span><span class="sxs-lookup"><span data-stu-id="5d370-126">-Id</span></span>
<span data-ttu-id="5d370-127">Anger ID för den resurs grupps distribution du vill stoppa.</span><span class="sxs-lookup"><span data-stu-id="5d370-127">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d370-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d370-128">-Name</span></span>
<span data-ttu-id="5d370-129">Anger namnet på den resurs grupps distribution du vill stoppa.</span><span class="sxs-lookup"><span data-stu-id="5d370-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="5d370-130">Om du inte anger den här parametern söker den här cmdleten efter en distribuerad distribution i resurs gruppen och stoppar den.</span><span class="sxs-lookup"><span data-stu-id="5d370-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="5d370-131">Om det finns fler än en distribuerad distribution Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="5d370-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="5d370-132">Använd Get-AzResourceGroupDeployment cmdlet för att få distributions namnet.</span><span class="sxs-lookup"><span data-stu-id="5d370-132">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d370-133">-För</span><span class="sxs-lookup"><span data-stu-id="5d370-133">-Pre</span></span>
<span data-ttu-id="5d370-134">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5d370-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5d370-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d370-135">-ResourceGroupName</span></span>
<span data-ttu-id="5d370-136">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5d370-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="5d370-137">Denna cmdlet stoppar distributionen av resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5d370-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d370-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d370-138">-Confirm</span></span>
<span data-ttu-id="5d370-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d370-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d370-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d370-140">-WhatIf</span></span>
<span data-ttu-id="5d370-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d370-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d370-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d370-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d370-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d370-143">CommonParameters</span></span>
<span data-ttu-id="5d370-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d370-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d370-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d370-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d370-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d370-146">INPUTS</span></span>

### <span data-ttu-id="5d370-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5d370-147">System.String</span></span>

## <span data-ttu-id="5d370-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d370-148">OUTPUTS</span></span>

### <span data-ttu-id="5d370-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d370-149">System.Boolean</span></span>

## <span data-ttu-id="5d370-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d370-150">NOTES</span></span>

## <span data-ttu-id="5d370-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d370-151">RELATED LINKS</span></span>

[<span data-ttu-id="5d370-152">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d370-152">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="5d370-153">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="5d370-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="5d370-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d370-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="5d370-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d370-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="5d370-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d370-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="5d370-157">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d370-157">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


