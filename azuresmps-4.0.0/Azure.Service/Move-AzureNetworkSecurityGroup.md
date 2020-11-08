---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099473"
---
# <span data-ttu-id="b6782-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6782-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="b6782-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6782-102">SYNOPSIS</span></span>
<span data-ttu-id="b6782-103">Migrerar en nätverks säkerhets grupp till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="b6782-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b6782-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6782-104">SYNTAX</span></span>

### <span data-ttu-id="b6782-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6782-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6782-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6782-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6782-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6782-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6782-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6782-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6782-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6782-109">DESCRIPTION</span></span>
<span data-ttu-id="b6782-110">Cmdleten **Move-AzureNetworkSecurityGroup** migrerar en nätverks säkerhets grupp till en resurs grupp i Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="b6782-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b6782-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6782-111">EXAMPLES</span></span>

### <span data-ttu-id="b6782-112">9.1</span><span class="sxs-lookup"><span data-stu-id="b6782-112">1:</span></span>
```

```

## <span data-ttu-id="b6782-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6782-113">PARAMETERS</span></span>

### <span data-ttu-id="b6782-114">-Avbryt</span><span class="sxs-lookup"><span data-stu-id="b6782-114">-Abort</span></span>
<span data-ttu-id="b6782-115">Anger att denna cmdlet avbryter migreringen av nätverks säkerhets grupper.</span><span class="sxs-lookup"><span data-stu-id="b6782-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="b6782-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="b6782-116">-Commit</span></span>
<span data-ttu-id="b6782-117">Anger att denna cmdlet startar nätverks säkerhets gruppmigreringen.</span><span class="sxs-lookup"><span data-stu-id="b6782-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="b6782-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b6782-118">-InformationAction</span></span>
<span data-ttu-id="b6782-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="b6782-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b6782-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b6782-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6782-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="b6782-121">Continue</span></span>
- <span data-ttu-id="b6782-122">Över</span><span class="sxs-lookup"><span data-stu-id="b6782-122">Ignore</span></span>
- <span data-ttu-id="b6782-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="b6782-123">Inquire</span></span>
- <span data-ttu-id="b6782-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b6782-124">SilentlyContinue</span></span>
- <span data-ttu-id="b6782-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="b6782-125">Stop</span></span>
- <span data-ttu-id="b6782-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="b6782-126">Suspend</span></span>

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

### <span data-ttu-id="b6782-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b6782-127">-InformationVariable</span></span>
<span data-ttu-id="b6782-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="b6782-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b6782-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="b6782-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="b6782-130">Anger namnet på den nätverks säkerhets grupp som denna cmdlet migrerar.</span><span class="sxs-lookup"><span data-stu-id="b6782-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="b6782-131">-Förbered</span><span class="sxs-lookup"><span data-stu-id="b6782-131">-Prepare</span></span>
<span data-ttu-id="b6782-132">Anger att denna cmdlet förbereder nätverks säkerhets gruppen för migrering.</span><span class="sxs-lookup"><span data-stu-id="b6782-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="b6782-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="b6782-133">-Profile</span></span>
<span data-ttu-id="b6782-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b6782-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6782-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b6782-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6782-136">-Validera</span><span class="sxs-lookup"><span data-stu-id="b6782-136">-Validate</span></span>
<span data-ttu-id="b6782-137">Anger att denna cmdlet verifierar nätverks säkerhets gruppen för migrering.</span><span class="sxs-lookup"><span data-stu-id="b6782-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="b6782-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6782-138">-Confirm</span></span>
<span data-ttu-id="b6782-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6782-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6782-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6782-140">-WhatIf</span></span>
<span data-ttu-id="b6782-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6782-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6782-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6782-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6782-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6782-143">CommonParameters</span></span>
<span data-ttu-id="b6782-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6782-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6782-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6782-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6782-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6782-146">INPUTS</span></span>

## <span data-ttu-id="b6782-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6782-147">OUTPUTS</span></span>

## <span data-ttu-id="b6782-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6782-148">NOTES</span></span>

## <span data-ttu-id="b6782-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6782-149">RELATED LINKS</span></span>

[<span data-ttu-id="b6782-150">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b6782-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="b6782-151">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6782-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="b6782-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="b6782-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="b6782-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6782-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="b6782-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6782-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


