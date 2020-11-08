---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099471"
---
# <span data-ttu-id="bb854-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bb854-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="bb854-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb854-102">SYNOPSIS</span></span>
<span data-ttu-id="bb854-103">Migrerar en väg tabell till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="bb854-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="bb854-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb854-104">SYNTAX</span></span>

### <span data-ttu-id="bb854-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb854-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb854-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb854-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb854-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb854-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb854-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb854-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb854-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb854-109">DESCRIPTION</span></span>
<span data-ttu-id="bb854-110">Cmdleten **Move-AzureRouteTable** migrerar en väg tabell till en resurs grupp i Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="bb854-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="bb854-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb854-111">EXAMPLES</span></span>

### <span data-ttu-id="bb854-112">9.1</span><span class="sxs-lookup"><span data-stu-id="bb854-112">1:</span></span>
```

```

## <span data-ttu-id="bb854-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb854-113">PARAMETERS</span></span>

### <span data-ttu-id="bb854-114">-Avbryt</span><span class="sxs-lookup"><span data-stu-id="bb854-114">-Abort</span></span>
<span data-ttu-id="bb854-115">Anger att denna cmdlet avbryter migreringen av väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="bb854-115">Indicates that this cmdlet cancels the route table migration.</span></span>

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

### <span data-ttu-id="bb854-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="bb854-116">-Commit</span></span>
<span data-ttu-id="bb854-117">Anger att den här cmdleten startar flyttning av route-tabell.</span><span class="sxs-lookup"><span data-stu-id="bb854-117">Indicates that this cmdlet starts the route table migration.</span></span>

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

### <span data-ttu-id="bb854-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bb854-118">-InformationAction</span></span>
<span data-ttu-id="bb854-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="bb854-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bb854-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bb854-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bb854-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="bb854-121">Continue</span></span>
- <span data-ttu-id="bb854-122">Över</span><span class="sxs-lookup"><span data-stu-id="bb854-122">Ignore</span></span>
- <span data-ttu-id="bb854-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="bb854-123">Inquire</span></span>
- <span data-ttu-id="bb854-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bb854-124">SilentlyContinue</span></span>
- <span data-ttu-id="bb854-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="bb854-125">Stop</span></span>
- <span data-ttu-id="bb854-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="bb854-126">Suspend</span></span>

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

### <span data-ttu-id="bb854-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bb854-127">-InformationVariable</span></span>
<span data-ttu-id="bb854-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="bb854-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bb854-129">-Förbered</span><span class="sxs-lookup"><span data-stu-id="bb854-129">-Prepare</span></span>
<span data-ttu-id="bb854-130">Anger att denna cmdlet förbereder väg tabellen för migrering.</span><span class="sxs-lookup"><span data-stu-id="bb854-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

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

### <span data-ttu-id="bb854-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="bb854-131">-Profile</span></span>
<span data-ttu-id="bb854-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="bb854-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bb854-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="bb854-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bb854-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="bb854-134">-RouteTableName</span></span>
<span data-ttu-id="bb854-135">Anger namnet på den routningstabell som denna cmdlet migrerar.</span><span class="sxs-lookup"><span data-stu-id="bb854-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="bb854-136">-Validera</span><span class="sxs-lookup"><span data-stu-id="bb854-136">-Validate</span></span>
<span data-ttu-id="bb854-137">Anger att denna cmdlet verifierar väg tabellen för migrering.</span><span class="sxs-lookup"><span data-stu-id="bb854-137">Specifies that this cmdlet validates the route table for migration.</span></span>

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

### <span data-ttu-id="bb854-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb854-138">-Confirm</span></span>
<span data-ttu-id="bb854-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb854-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb854-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb854-140">-WhatIf</span></span>
<span data-ttu-id="bb854-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb854-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb854-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb854-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb854-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb854-143">CommonParameters</span></span>
<span data-ttu-id="bb854-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb854-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb854-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb854-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb854-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb854-146">INPUTS</span></span>

## <span data-ttu-id="bb854-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb854-147">OUTPUTS</span></span>

## <span data-ttu-id="bb854-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb854-148">NOTES</span></span>

## <span data-ttu-id="bb854-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb854-149">RELATED LINKS</span></span>

[<span data-ttu-id="bb854-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bb854-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="bb854-151">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="bb854-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="bb854-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="bb854-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="bb854-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb854-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="bb854-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb854-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


