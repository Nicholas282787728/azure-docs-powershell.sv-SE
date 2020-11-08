---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099468"
---
# <span data-ttu-id="3f62e-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3f62e-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="3f62e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f62e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f62e-103">Migrerar ett virtuellt nätverk till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="3f62e-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="3f62e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f62e-104">SYNTAX</span></span>

### <span data-ttu-id="3f62e-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f62e-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f62e-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f62e-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f62e-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f62e-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f62e-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f62e-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f62e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f62e-109">DESCRIPTION</span></span>
<span data-ttu-id="3f62e-110">Cmdleten **Move-AzureVirtualNetwork** migrerar ett virtuellt nätverk till en resurs grupp i Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="3f62e-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="3f62e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f62e-111">EXAMPLES</span></span>

### <span data-ttu-id="3f62e-112">Exempel 1: förbereda virtuell nätverkskommunikation</span><span class="sxs-lookup"><span data-stu-id="3f62e-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="3f62e-113">Det här kommandot förbereder det virtuella nätverket med namnet ContosoVNET för migrering till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="3f62e-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="3f62e-114">Exempel 2: starta virtuell nätverkskommunikation</span><span class="sxs-lookup"><span data-stu-id="3f62e-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="3f62e-115">Det här kommandot börjar migrera det virtuella nätverk som heter ContosoVNET till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="3f62e-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="3f62e-116">Exempel 3: verifiera virtuell nätverkskommunikation</span><span class="sxs-lookup"><span data-stu-id="3f62e-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="3f62e-117">Det här kommandot verifierar migrering för det virtuella nätverk som heter ContosoVNET till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="3f62e-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="3f62e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f62e-118">PARAMETERS</span></span>

### <span data-ttu-id="3f62e-119">-Avbryt</span><span class="sxs-lookup"><span data-stu-id="3f62e-119">-Abort</span></span>
<span data-ttu-id="3f62e-120">Anger att denna cmdlet avbryter den virtuella nätverks migreringen.</span><span class="sxs-lookup"><span data-stu-id="3f62e-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

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

### <span data-ttu-id="3f62e-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="3f62e-121">-Commit</span></span>
<span data-ttu-id="3f62e-122">Anger att den här cmdleten startar virtuell nätverkskommunikation.</span><span class="sxs-lookup"><span data-stu-id="3f62e-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

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

### <span data-ttu-id="3f62e-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3f62e-123">-InformationAction</span></span>
<span data-ttu-id="3f62e-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3f62e-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3f62e-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3f62e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f62e-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="3f62e-126">Continue</span></span>
- <span data-ttu-id="3f62e-127">Över</span><span class="sxs-lookup"><span data-stu-id="3f62e-127">Ignore</span></span>
- <span data-ttu-id="3f62e-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="3f62e-128">Inquire</span></span>
- <span data-ttu-id="3f62e-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f62e-129">SilentlyContinue</span></span>
- <span data-ttu-id="3f62e-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="3f62e-130">Stop</span></span>
- <span data-ttu-id="3f62e-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3f62e-131">Suspend</span></span>

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

### <span data-ttu-id="3f62e-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f62e-132">-InformationVariable</span></span>
<span data-ttu-id="3f62e-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3f62e-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3f62e-134">-Förbered</span><span class="sxs-lookup"><span data-stu-id="3f62e-134">-Prepare</span></span>
<span data-ttu-id="3f62e-135">Anger att denna cmdlet förbereder det virtuella nätverket för migrering.</span><span class="sxs-lookup"><span data-stu-id="3f62e-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62e-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f62e-136">-Profile</span></span>
<span data-ttu-id="3f62e-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3f62e-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f62e-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3f62e-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f62e-139">-Validera</span><span class="sxs-lookup"><span data-stu-id="3f62e-139">-Validate</span></span>
<span data-ttu-id="3f62e-140">Anger att denna cmdlet verifierar det virtuella nätverket för migrering.</span><span class="sxs-lookup"><span data-stu-id="3f62e-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62e-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3f62e-141">-VirtualNetworkName</span></span>
<span data-ttu-id="3f62e-142">Namn på det virtuella nätverk som ska migreras</span><span class="sxs-lookup"><span data-stu-id="3f62e-142">Name of the Virtual Network to migrate</span></span>

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

### <span data-ttu-id="3f62e-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f62e-143">-Confirm</span></span>
<span data-ttu-id="3f62e-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f62e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f62e-145">-WhatIf</span></span>
<span data-ttu-id="3f62e-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f62e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f62e-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f62e-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f62e-148">CommonParameters</span></span>
<span data-ttu-id="3f62e-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f62e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f62e-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f62e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f62e-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f62e-151">INPUTS</span></span>

## <span data-ttu-id="3f62e-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f62e-152">OUTPUTS</span></span>

## <span data-ttu-id="3f62e-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f62e-153">NOTES</span></span>

## <span data-ttu-id="3f62e-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f62e-154">RELATED LINKS</span></span>

[<span data-ttu-id="3f62e-155">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3f62e-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="3f62e-156">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3f62e-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="3f62e-157">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f62e-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="3f62e-158">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="3f62e-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="3f62e-159">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f62e-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


