---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099343"
---
# <span data-ttu-id="41ebb-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="41ebb-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="41ebb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="41ebb-103">Tar bort moln tjänst tillägg som används vid en distribution.</span><span class="sxs-lookup"><span data-stu-id="41ebb-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="41ebb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41ebb-104">SYNTAX</span></span>

### <span data-ttu-id="41ebb-105">RemoveByRoles (standard)</span><span class="sxs-lookup"><span data-stu-id="41ebb-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="41ebb-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="41ebb-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="41ebb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41ebb-107">DESCRIPTION</span></span>
<span data-ttu-id="41ebb-108">Cmdleten **Remove-AzureServiceExtension** tar bort moln tjänst tillägg som tillämpas på en distribution.</span><span class="sxs-lookup"><span data-stu-id="41ebb-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="41ebb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41ebb-109">EXAMPLES</span></span>

### <span data-ttu-id="41ebb-110">Exempel 1: ta bort en tjänst anknytning</span><span class="sxs-lookup"><span data-stu-id="41ebb-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="41ebb-111">Det här kommandot tar bort en tjänst anknytning.</span><span class="sxs-lookup"><span data-stu-id="41ebb-111">This command removes a service extension.</span></span>

### <span data-ttu-id="41ebb-112">Exempel 2: ta bort en tjänst förlängning och avinstallera alla konfigurationer</span><span class="sxs-lookup"><span data-stu-id="41ebb-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="41ebb-113">Det här kommandot tar bort en tjänst anknytning och avinstallerar alla konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="41ebb-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="41ebb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41ebb-114">PARAMETERS</span></span>

### <span data-ttu-id="41ebb-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="41ebb-115">-ExtensionName</span></span>
<span data-ttu-id="41ebb-116">Anger tillägget.</span><span class="sxs-lookup"><span data-stu-id="41ebb-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41ebb-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="41ebb-117">-InformationAction</span></span>
<span data-ttu-id="41ebb-118">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="41ebb-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41ebb-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="41ebb-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41ebb-120">Vidare</span><span class="sxs-lookup"><span data-stu-id="41ebb-120">Continue</span></span>
- <span data-ttu-id="41ebb-121">Över</span><span class="sxs-lookup"><span data-stu-id="41ebb-121">Ignore</span></span>
- <span data-ttu-id="41ebb-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="41ebb-122">Inquire</span></span>
- <span data-ttu-id="41ebb-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41ebb-123">SilentlyContinue</span></span>
- <span data-ttu-id="41ebb-124">Stanna</span><span class="sxs-lookup"><span data-stu-id="41ebb-124">Stop</span></span>
- <span data-ttu-id="41ebb-125">Avbryt</span><span class="sxs-lookup"><span data-stu-id="41ebb-125">Suspend</span></span>

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

### <span data-ttu-id="41ebb-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41ebb-126">-InformationVariable</span></span>
<span data-ttu-id="41ebb-127">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="41ebb-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="41ebb-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="41ebb-128">-Profile</span></span>
<span data-ttu-id="41ebb-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="41ebb-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41ebb-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="41ebb-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41ebb-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="41ebb-131">-ProviderNamespace</span></span>
<span data-ttu-id="41ebb-132">Anger namn området för tilläggs leverantör.</span><span class="sxs-lookup"><span data-stu-id="41ebb-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41ebb-133">-Roll</span><span class="sxs-lookup"><span data-stu-id="41ebb-133">-Role</span></span>
<span data-ttu-id="41ebb-134">Anger en valfri uppsättning roller för att ange fil namns tillägget för.</span><span class="sxs-lookup"><span data-stu-id="41ebb-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="41ebb-135">Om du inte anger alternativet används tillägget som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="41ebb-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="41ebb-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="41ebb-136">-ServiceName</span></span>
<span data-ttu-id="41ebb-137">Anger moln tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="41ebb-137">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="41ebb-138">-Plats</span><span class="sxs-lookup"><span data-stu-id="41ebb-138">-Slot</span></span>
<span data-ttu-id="41ebb-139">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="41ebb-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="41ebb-140">Giltiga värden är produktion eller för produktion.</span><span class="sxs-lookup"><span data-stu-id="41ebb-140">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="41ebb-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="41ebb-141">-UninstallConfiguration</span></span>
<span data-ttu-id="41ebb-142">Anger att denna cmdlet avinstallerar alla konfigurationer från moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="41ebb-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ebb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ebb-143">CommonParameters</span></span>
<span data-ttu-id="41ebb-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ebb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ebb-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ebb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ebb-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41ebb-146">INPUTS</span></span>

## <span data-ttu-id="41ebb-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41ebb-147">OUTPUTS</span></span>

## <span data-ttu-id="41ebb-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41ebb-148">NOTES</span></span>

## <span data-ttu-id="41ebb-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41ebb-149">RELATED LINKS</span></span>

[<span data-ttu-id="41ebb-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="41ebb-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="41ebb-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="41ebb-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


