---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099356"
---
# <span data-ttu-id="6bc3f-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6bc3f-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="6bc3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bc3f-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc3f-103">Tar bort tillägget moln tjänstens AD-domän som tillämpas på alla roller eller namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="6bc3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bc3f-104">SYNTAX</span></span>

### <span data-ttu-id="6bc3f-105">RemoveByRoles (standard)</span><span class="sxs-lookup"><span data-stu-id="6bc3f-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6bc3f-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="6bc3f-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bc3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bc3f-107">DESCRIPTION</span></span>
<span data-ttu-id="6bc3f-108">Cmdleten **Remove-AzureServiceADDomainExtension** tar bort den molnbaserade Active Directory-domänen (AD) som tillämpas på alla roller eller namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="6bc3f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bc3f-109">EXAMPLES</span></span>

### <span data-ttu-id="6bc3f-110">Exempel 1: ta bort ett AD-domännätverk</span><span class="sxs-lookup"><span data-stu-id="6bc3f-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="6bc3f-111">Det här kommandot tar bort tillägget som anges av variabeln $Svc.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="6bc3f-112">Exempel 2: ta bort ett AD-domännätverk för en viss roll</span><span class="sxs-lookup"><span data-stu-id="6bc3f-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="6bc3f-113">Det här kommandot tar bort tjänst tillägget för den angivna rollen.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="6bc3f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bc3f-114">PARAMETERS</span></span>

### <span data-ttu-id="6bc3f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6bc3f-115">-InformationAction</span></span>
<span data-ttu-id="6bc3f-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6bc3f-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6bc3f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6bc3f-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="6bc3f-118">Continue</span></span>
- <span data-ttu-id="6bc3f-119">Över</span><span class="sxs-lookup"><span data-stu-id="6bc3f-119">Ignore</span></span>
- <span data-ttu-id="6bc3f-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="6bc3f-120">Inquire</span></span>
- <span data-ttu-id="6bc3f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6bc3f-121">SilentlyContinue</span></span>
- <span data-ttu-id="6bc3f-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="6bc3f-122">Stop</span></span>
- <span data-ttu-id="6bc3f-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6bc3f-123">Suspend</span></span>

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

### <span data-ttu-id="6bc3f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6bc3f-124">-InformationVariable</span></span>
<span data-ttu-id="6bc3f-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6bc3f-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="6bc3f-126">-Profile</span></span>
<span data-ttu-id="6bc3f-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6bc3f-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6bc3f-129">-Roll</span><span class="sxs-lookup"><span data-stu-id="6bc3f-129">-Role</span></span>
<span data-ttu-id="6bc3f-130">Anger en valfri matris med roller som du kan ange fjärr skrivbords konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="6bc3f-131">Om inget anges används AD-domänens konfiguration som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc3f-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6bc3f-132">-ServiceName</span></span>
<span data-ttu-id="6bc3f-133">Anger namnet på en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-133">Specifies the name of an Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc3f-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="6bc3f-134">-Slot</span></span>
<span data-ttu-id="6bc3f-135">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="6bc3f-136">Giltiga värden är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-136">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="6bc3f-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bc3f-137">-UninstallConfiguration</span></span>
<span data-ttu-id="6bc3f-138">Anger att denna cmdlet avinstallerar alla AD-domänsuffix från moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc3f-139">CommonParameters</span></span>
<span data-ttu-id="6bc3f-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bc3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc3f-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bc3f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc3f-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bc3f-142">INPUTS</span></span>

## <span data-ttu-id="6bc3f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bc3f-143">OUTPUTS</span></span>

## <span data-ttu-id="6bc3f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bc3f-144">NOTES</span></span>

## <span data-ttu-id="6bc3f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bc3f-145">RELATED LINKS</span></span>

[<span data-ttu-id="6bc3f-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6bc3f-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="6bc3f-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6bc3f-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


