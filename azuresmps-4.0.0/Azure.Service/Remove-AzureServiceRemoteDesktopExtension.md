---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099342"
---
# <span data-ttu-id="a6526-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="a6526-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="a6526-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6526-102">SYNOPSIS</span></span>
<span data-ttu-id="a6526-103">Tar bort moln tjänst tillägget fjärr skrivbord som tillämpas på alla roller eller namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="a6526-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="a6526-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6526-104">SYNTAX</span></span>

### <span data-ttu-id="a6526-105">RemoveByRoles (standard)</span><span class="sxs-lookup"><span data-stu-id="a6526-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6526-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="a6526-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a6526-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6526-107">DESCRIPTION</span></span>
<span data-ttu-id="a6526-108">Cmdleten **Remove-AzureServiceRemoteDesktopExtension** tar bort moln tjänstens fil tillägg för fjärr skrivbord som tillämpas på alla roller eller med namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="a6526-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="a6526-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6526-109">EXAMPLES</span></span>

### <span data-ttu-id="a6526-110">Exempel 1: ta bort fjärr skrivbords tillägget</span><span class="sxs-lookup"><span data-stu-id="a6526-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="a6526-111">Det här kommandot tar bort tillägget fjärr skrivbord.</span><span class="sxs-lookup"><span data-stu-id="a6526-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="a6526-112">Exempel 2: ta bort fjärr skrivbords tillägget från en viss roll</span><span class="sxs-lookup"><span data-stu-id="a6526-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="a6526-113">Det här kommandot tar bort tillägget fjärr skrivbord från en angiven roll.</span><span class="sxs-lookup"><span data-stu-id="a6526-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="a6526-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6526-114">PARAMETERS</span></span>

### <span data-ttu-id="a6526-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a6526-115">-InformationAction</span></span>
<span data-ttu-id="a6526-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a6526-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a6526-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a6526-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a6526-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="a6526-118">Continue</span></span>
- <span data-ttu-id="a6526-119">Över</span><span class="sxs-lookup"><span data-stu-id="a6526-119">Ignore</span></span>
- <span data-ttu-id="a6526-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="a6526-120">Inquire</span></span>
- <span data-ttu-id="a6526-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a6526-121">SilentlyContinue</span></span>
- <span data-ttu-id="a6526-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="a6526-122">Stop</span></span>
- <span data-ttu-id="a6526-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a6526-123">Suspend</span></span>

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

### <span data-ttu-id="a6526-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a6526-124">-InformationVariable</span></span>
<span data-ttu-id="a6526-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a6526-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a6526-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="a6526-126">-Profile</span></span>
<span data-ttu-id="a6526-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a6526-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a6526-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a6526-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6526-129">-Roll</span><span class="sxs-lookup"><span data-stu-id="a6526-129">-Role</span></span>
<span data-ttu-id="a6526-130">Anger en valfri uppsättning roller för att ange fjärr skrivbords konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="a6526-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="a6526-131">Om du inte anger konfigurationen för fjärr skrivbord används som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="a6526-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="a6526-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a6526-132">-ServiceName</span></span>
<span data-ttu-id="a6526-133">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a6526-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="a6526-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="a6526-134">-Slot</span></span>
<span data-ttu-id="a6526-135">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="a6526-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="a6526-136">Värden som stöds är "produktion" eller "mellanlagring".</span><span class="sxs-lookup"><span data-stu-id="a6526-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="a6526-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6526-137">-UninstallConfiguration</span></span>
<span data-ttu-id="a6526-138">Anger att denna cmdlet avinstallerar alla RDP-konfigurationer från moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a6526-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="a6526-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6526-139">CommonParameters</span></span>
<span data-ttu-id="a6526-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6526-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6526-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6526-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6526-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6526-142">INPUTS</span></span>

## <span data-ttu-id="a6526-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6526-143">OUTPUTS</span></span>

## <span data-ttu-id="a6526-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6526-144">NOTES</span></span>

## <span data-ttu-id="a6526-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6526-145">RELATED LINKS</span></span>

[<span data-ttu-id="a6526-146">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="a6526-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


