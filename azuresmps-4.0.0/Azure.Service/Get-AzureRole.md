---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099544"
---
# <span data-ttu-id="b8cc5-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="b8cc5-101">Get-AzureRole</span></span>

## <span data-ttu-id="b8cc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="b8cc5-103">Returnerar en lista med roller i Microsoft Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="b8cc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8cc5-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8cc5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="b8cc5-106">Cmdleten **Get-AzureRole** returnerar ett List objekt med information om rollerna i Microsoft Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="b8cc5-107">Om du anger parametern *rolename* returnerar **AzureRole** bara uppgifter för den rollen.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="b8cc5-108">Om du anger parametern *InstanceDetails* returneras ytterligare instans information.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="b8cc5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8cc5-109">EXAMPLES</span></span>

### <span data-ttu-id="b8cc5-110">Exempel 1: Visa en lista över roller för en tjänst</span><span class="sxs-lookup"><span data-stu-id="b8cc5-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="b8cc5-111">Det här kommandot returnerar ett objekt med information om alla produktions roller som körs på MySvc01-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="b8cc5-112">Exempel 2: få information om en roll som körs på en tjänst</span><span class="sxs-lookup"><span data-stu-id="b8cc5-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="b8cc5-113">Det här kommandot returnerar ett objekt med information om MyTestVM3-rollen som körs i mellanlagringsdatabasen för MySvc01-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="b8cc5-114">Exempel 3: Hämta instans information om instanser av en roll som körs på en tjänst</span><span class="sxs-lookup"><span data-stu-id="b8cc5-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="b8cc5-115">Det här kommandot returnerar ett objekt med information om MyTestVM02-rollen som körs i produktions miljön på MySvc01-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="b8cc5-116">Exempel 4: Hämta en tabell med roll instanser kopplade till en tjänst</span><span class="sxs-lookup"><span data-stu-id="b8cc5-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="b8cc5-117">Det här kommandot returnerar en tabell med instansens namn, storlek och status för alla roll instanser som körs i produktions miljön på MySvc01-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="b8cc5-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8cc5-118">PARAMETERS</span></span>

### <span data-ttu-id="b8cc5-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8cc5-119">-InformationAction</span></span>
<span data-ttu-id="b8cc5-120">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8cc5-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b8cc5-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8cc5-122">Vidare</span><span class="sxs-lookup"><span data-stu-id="b8cc5-122">Continue</span></span>
- <span data-ttu-id="b8cc5-123">Över</span><span class="sxs-lookup"><span data-stu-id="b8cc5-123">Ignore</span></span>
- <span data-ttu-id="b8cc5-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="b8cc5-124">Inquire</span></span>
- <span data-ttu-id="b8cc5-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8cc5-125">SilentlyContinue</span></span>
- <span data-ttu-id="b8cc5-126">Stanna</span><span class="sxs-lookup"><span data-stu-id="b8cc5-126">Stop</span></span>
- <span data-ttu-id="b8cc5-127">Avbryt</span><span class="sxs-lookup"><span data-stu-id="b8cc5-127">Suspend</span></span>

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

### <span data-ttu-id="b8cc5-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8cc5-128">-InformationVariable</span></span>
<span data-ttu-id="b8cc5-129">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b8cc5-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="b8cc5-130">-InstanceDetails</span></span>
<span data-ttu-id="b8cc5-131">Anger att den här cmdleten returnerar information om instanser för varje roll.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cc5-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="b8cc5-132">-Profile</span></span>
<span data-ttu-id="b8cc5-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8cc5-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8cc5-135">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b8cc5-135">-RoleName</span></span>
<span data-ttu-id="b8cc5-136">Anger namnet på den roll som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cc5-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b8cc5-137">-ServiceName</span></span>
<span data-ttu-id="b8cc5-138">Anger namnet på Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-138">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cc5-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="b8cc5-139">-Slot</span></span>
<span data-ttu-id="b8cc5-140">Anger Azure Deployment Environment.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="b8cc5-141">De acceptabla värdena för denna parameter är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-141">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cc5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8cc5-142">CommonParameters</span></span>
<span data-ttu-id="b8cc5-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8cc5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8cc5-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8cc5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8cc5-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8cc5-145">INPUTS</span></span>

## <span data-ttu-id="b8cc5-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8cc5-146">OUTPUTS</span></span>

## <span data-ttu-id="b8cc5-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8cc5-147">NOTES</span></span>

## <span data-ttu-id="b8cc5-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8cc5-148">RELATED LINKS</span></span>

[<span data-ttu-id="b8cc5-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="b8cc5-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


