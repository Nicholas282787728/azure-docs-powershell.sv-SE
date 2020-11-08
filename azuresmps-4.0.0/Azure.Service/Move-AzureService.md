---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099470"
---
# <span data-ttu-id="a8fef-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="a8fef-101">Move-AzureService</span></span>

## <span data-ttu-id="a8fef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8fef-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fef-103">Migrerar en moln tjänst till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a8fef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8fef-104">SYNTAX</span></span>

### <span data-ttu-id="a8fef-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8fef-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8fef-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8fef-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8fef-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8fef-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8fef-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8fef-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8fef-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8fef-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8fef-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8fef-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8fef-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8fef-111">DESCRIPTION</span></span>
<span data-ttu-id="a8fef-112">Cmdleten **Move-AzureService** migrerar en moln tjänst och en distribution i den tjänsten till en resurs grupp i Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a8fef-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8fef-113">EXAMPLES</span></span>

### <span data-ttu-id="a8fef-114">Exempel 1: förbereda tjänste migration</span><span class="sxs-lookup"><span data-stu-id="a8fef-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="a8fef-115">Det här kommandot förbereder tjänsten ContosoService för migrering till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a8fef-116">Migreringen inkluderar distributionen med namnet ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="a8fef-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a8fef-117">Exempel 2: starta tjänste migration</span><span class="sxs-lookup"><span data-stu-id="a8fef-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="a8fef-118">Det här kommandot startar migrering av tjänsten med namnet ContosoService till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a8fef-119">Migreringen inkluderar distributionen med namnet ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="a8fef-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a8fef-120">Exempel 3: Avbryt migrering av tjänst</span><span class="sxs-lookup"><span data-stu-id="a8fef-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="a8fef-121">Det här kommandot avbryter migrering av tjänsten som heter ContosoService till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="a8fef-122">Exempel 4: förbereda tjänste migrering till ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="a8fef-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="a8fef-123">Det här kommandot förbereder tjänsten ContosoService för migrering till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a8fef-124">Migreringen inkluderar distributionen med namnet ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="a8fef-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="a8fef-125">Migreringen använder ett virtuellt nätverk som redan har skapats.</span><span class="sxs-lookup"><span data-stu-id="a8fef-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="a8fef-126">Exempel 5: verifiera tjänst migration</span><span class="sxs-lookup"><span data-stu-id="a8fef-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="a8fef-127">Det här kommandot verifierar migrering för tjänsten som heter ContosoService till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a8fef-128">Migreringen inkluderar distributionen med namnet ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="a8fef-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a8fef-129">Exempel 6: verifiera tjänst migrering till ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="a8fef-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="a8fef-130">Det här kommandot verifierar migrering för tjänsten som heter ContosoService till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a8fef-131">Migreringen inkluderar distributionen med namnet ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="a8fef-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="a8fef-132">Migreringen använder ett virtuellt nätverk som redan har skapats.</span><span class="sxs-lookup"><span data-stu-id="a8fef-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="a8fef-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8fef-133">PARAMETERS</span></span>

### <span data-ttu-id="a8fef-134">-Avbryt</span><span class="sxs-lookup"><span data-stu-id="a8fef-134">-Abort</span></span>
<span data-ttu-id="a8fef-135">Anger att denna cmdlet avbryter tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a8fef-135">Indicates that this cmdlet cancels the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-136">-Commit</span><span class="sxs-lookup"><span data-stu-id="a8fef-136">-Commit</span></span>
<span data-ttu-id="a8fef-137">Anger att den här cmdleten startar tjänstens migrering.</span><span class="sxs-lookup"><span data-stu-id="a8fef-137">Indicates that this cmdlet starts the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8fef-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="a8fef-139">Anger att den här cmdleten skapar ett virtuellt nätverk i Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-140">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a8fef-140">-DeploymentName</span></span>
<span data-ttu-id="a8fef-141">Anger namnet på den moln tjänst distribution som denna cmdlet migrerar.</span><span class="sxs-lookup"><span data-stu-id="a8fef-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-142">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a8fef-142">-InformationAction</span></span>
<span data-ttu-id="a8fef-143">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a8fef-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a8fef-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a8fef-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8fef-145">Vidare</span><span class="sxs-lookup"><span data-stu-id="a8fef-145">Continue</span></span>
- <span data-ttu-id="a8fef-146">Över</span><span class="sxs-lookup"><span data-stu-id="a8fef-146">Ignore</span></span>
- <span data-ttu-id="a8fef-147">Inquire</span><span class="sxs-lookup"><span data-stu-id="a8fef-147">Inquire</span></span>
- <span data-ttu-id="a8fef-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a8fef-148">SilentlyContinue</span></span>
- <span data-ttu-id="a8fef-149">Stanna</span><span class="sxs-lookup"><span data-stu-id="a8fef-149">Stop</span></span>
- <span data-ttu-id="a8fef-150">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a8fef-150">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a8fef-151">-InformationVariable</span></span>
<span data-ttu-id="a8fef-152">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a8fef-152">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-153">-Förbered</span><span class="sxs-lookup"><span data-stu-id="a8fef-153">-Prepare</span></span>
<span data-ttu-id="a8fef-154">Anger att denna cmdlet förbereder moln tjänsten för migrering.</span><span class="sxs-lookup"><span data-stu-id="a8fef-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8fef-155">-Profile</span></span>
<span data-ttu-id="a8fef-156">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a8fef-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8fef-157">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a8fef-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a8fef-158">-ServiceName</span></span>
<span data-ttu-id="a8fef-159">Anger namnet på den moln tjänst som denna cmdlet migrerar.</span><span class="sxs-lookup"><span data-stu-id="a8fef-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a8fef-160">-SubnetName</span></span>
<span data-ttu-id="a8fef-161">Anger namnet på under nätet i det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="a8fef-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8fef-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="a8fef-163">Anger att denna cmdlet migrerar moln tjänsten till ett befintligt virtuellt nätverk i Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="a8fef-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-164">-Validera</span><span class="sxs-lookup"><span data-stu-id="a8fef-164">-Validate</span></span>
<span data-ttu-id="a8fef-165">Anger att denna cmdlet verifierar moln tjänsten för migrering.</span><span class="sxs-lookup"><span data-stu-id="a8fef-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a8fef-166">-VirtualNetworkName</span></span>
<span data-ttu-id="a8fef-167">Anger namnet på ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="a8fef-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8fef-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="a8fef-169">Anger namnet på resurs gruppen för ett befintligt virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="a8fef-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fef-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8fef-170">CommonParameters</span></span>
<span data-ttu-id="a8fef-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8fef-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8fef-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8fef-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8fef-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8fef-173">INPUTS</span></span>

## <span data-ttu-id="a8fef-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8fef-174">OUTPUTS</span></span>

## <span data-ttu-id="a8fef-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8fef-175">NOTES</span></span>

## <span data-ttu-id="a8fef-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8fef-176">RELATED LINKS</span></span>

[<span data-ttu-id="a8fef-177">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8fef-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="a8fef-178">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="a8fef-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="a8fef-179">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8fef-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="a8fef-180">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8fef-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="a8fef-181">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8fef-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


