---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099346"
---
# <span data-ttu-id="e24b8-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e24b8-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="e24b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e24b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e24b8-103">Tar bort tillägget för tillägg för moln tjänsten som tillämpas på alla roller eller namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="e24b8-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="e24b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e24b8-104">SYNTAX</span></span>

### <span data-ttu-id="e24b8-105">RemoveByRoles (standard)</span><span class="sxs-lookup"><span data-stu-id="e24b8-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e24b8-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="e24b8-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e24b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e24b8-107">DESCRIPTION</span></span>
<span data-ttu-id="e24b8-108">Cmdleten **Remove-AzureServiceDiagnosticsExtension** tar bort tillägget för tillägg för tillägg som tillämpas på alla roller eller namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="e24b8-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="e24b8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e24b8-109">EXAMPLES</span></span>

### <span data-ttu-id="e24b8-110">Exempel 1: ta bort diagnos tillägget för en tjänst</span><span class="sxs-lookup"><span data-stu-id="e24b8-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="e24b8-111">Det här kommandot tar bort diagnos tillägget för en viss roll.</span><span class="sxs-lookup"><span data-stu-id="e24b8-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="e24b8-112">Exempel 2: ta bort diagnos tillägget för en tjänst i en viss roll</span><span class="sxs-lookup"><span data-stu-id="e24b8-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="e24b8-113">Det här kommandot tar bort diagnos tillägget för en viss roll.</span><span class="sxs-lookup"><span data-stu-id="e24b8-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="e24b8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e24b8-114">PARAMETERS</span></span>

### <span data-ttu-id="e24b8-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e24b8-115">-InformationAction</span></span>
<span data-ttu-id="e24b8-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e24b8-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e24b8-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e24b8-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e24b8-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="e24b8-118">Continue</span></span>
- <span data-ttu-id="e24b8-119">Över</span><span class="sxs-lookup"><span data-stu-id="e24b8-119">Ignore</span></span>
- <span data-ttu-id="e24b8-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="e24b8-120">Inquire</span></span>
- <span data-ttu-id="e24b8-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e24b8-121">SilentlyContinue</span></span>
- <span data-ttu-id="e24b8-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="e24b8-122">Stop</span></span>
- <span data-ttu-id="e24b8-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e24b8-123">Suspend</span></span>

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

### <span data-ttu-id="e24b8-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e24b8-124">-InformationVariable</span></span>
<span data-ttu-id="e24b8-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e24b8-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e24b8-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="e24b8-126">-Profile</span></span>
<span data-ttu-id="e24b8-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e24b8-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e24b8-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e24b8-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e24b8-129">-Roll</span><span class="sxs-lookup"><span data-stu-id="e24b8-129">-Role</span></span>
<span data-ttu-id="e24b8-130">Anger en valfri matris med roller som du kan ange fjärr skrivbords konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="e24b8-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="e24b8-131">Om du inte anger den här parametern används fjärr skrivbords konfigurationen som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="e24b8-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="e24b8-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e24b8-132">-ServiceName</span></span>
<span data-ttu-id="e24b8-133">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e24b8-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="e24b8-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="e24b8-134">-Slot</span></span>
<span data-ttu-id="e24b8-135">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e24b8-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="e24b8-136">Giltiga värden är produktion eller för produktion.</span><span class="sxs-lookup"><span data-stu-id="e24b8-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="e24b8-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e24b8-137">-UninstallConfiguration</span></span>
<span data-ttu-id="e24b8-138">Anger att denna cmdlet avinstallerar alla RDP-konfigurationer från moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e24b8-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="e24b8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24b8-139">CommonParameters</span></span>
<span data-ttu-id="e24b8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e24b8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24b8-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e24b8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24b8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e24b8-142">INPUTS</span></span>

## <span data-ttu-id="e24b8-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e24b8-143">OUTPUTS</span></span>

## <span data-ttu-id="e24b8-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e24b8-144">NOTES</span></span>

## <span data-ttu-id="e24b8-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e24b8-145">RELATED LINKS</span></span>

[<span data-ttu-id="e24b8-146">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e24b8-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="e24b8-147">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e24b8-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


