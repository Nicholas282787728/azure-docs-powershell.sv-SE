---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093206"
---
# <span data-ttu-id="167e0-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="167e0-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="167e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="167e0-102">SYNOPSIS</span></span>
<span data-ttu-id="167e0-103">Begär en omstart eller återbildning av en enskild roll instans eller alla roll instanser för en viss roll.</span><span class="sxs-lookup"><span data-stu-id="167e0-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="167e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="167e0-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="167e0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="167e0-105">DESCRIPTION</span></span>
<span data-ttu-id="167e0-106">Cmdleten **Reset-AzureRoleInstance** begär en omstart eller en bild av en roll instans som körs i en distribution.</span><span class="sxs-lookup"><span data-stu-id="167e0-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="167e0-107">Den här åtgärden körs synkront.</span><span class="sxs-lookup"><span data-stu-id="167e0-107">This operation executes synchronously.</span></span>
<span data-ttu-id="167e0-108">När du startar om en roll instans använder Azure instansen offline, startar om det underliggande operativ systemet för den instansen och ansluter sedan till instansen online.</span><span class="sxs-lookup"><span data-stu-id="167e0-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="167e0-109">Alla data som skrivs till den lokala disken fortsätter att starta om.</span><span class="sxs-lookup"><span data-stu-id="167e0-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="167e0-110">Alla data som finns i minnet förloras.</span><span class="sxs-lookup"><span data-stu-id="167e0-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="167e0-111">Om en roll instans rebildas beror olika beteende beroende på typen av roll.</span><span class="sxs-lookup"><span data-stu-id="167e0-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="167e0-112">När rollen ändras för en webb-eller arbets roll använder Azure rollen offline och skriver en ny installation av Azure gäst operativ systemet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="167e0-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="167e0-113">Rollen ansluts sedan online igen.</span><span class="sxs-lookup"><span data-stu-id="167e0-113">The role is then brought back online.</span></span>
<span data-ttu-id="167e0-114">För en virtuell dator roll använder Azure rollen offline när du har angett den för att den ska kopplas från, så återanvänds den anpassade avbildningen som du har tillhandahållit.</span><span class="sxs-lookup"><span data-stu-id="167e0-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="167e0-115">Azure försöker upprätthålla data från alla lokala lagrings resurser när rollen är ombildad; om det däremot inte uppstår något fel kan den lokala lagrings resursen gå förlorad.</span><span class="sxs-lookup"><span data-stu-id="167e0-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="167e0-116">Om ditt program kräver att data bevaras kan det vara bra att skriva till en hållbar data källa, till exempel en Azure-enhet.</span><span class="sxs-lookup"><span data-stu-id="167e0-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="167e0-117">Alla data som skrivs till en annan lokal katalog än den som definieras av den lokala lagrings resursen försvinner när rollen ändras.</span><span class="sxs-lookup"><span data-stu-id="167e0-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="167e0-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="167e0-118">EXAMPLES</span></span>

### <span data-ttu-id="167e0-119">Exempel 1: starta om en roll instans</span><span class="sxs-lookup"><span data-stu-id="167e0-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="167e0-120">Det här kommandot startar om den roll instans som heter MyWebRole_IN_0 i den mellanliggande distributionen av MySvc01-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="167e0-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="167e0-121">Exempel 2: återpå en roll instans</span><span class="sxs-lookup"><span data-stu-id="167e0-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="167e0-122">Det här kommandot återavbildningar roll instanser för mellanlagring av MySvc01-moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="167e0-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="167e0-123">Exempel 3: återbild alla roll instanser</span><span class="sxs-lookup"><span data-stu-id="167e0-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="167e0-124">Det här kommandot återavbildningar alla roll instanser i produktions distributionen av MySvc01-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="167e0-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="167e0-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="167e0-125">PARAMETERS</span></span>

### <span data-ttu-id="167e0-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="167e0-126">-InformationAction</span></span>
<span data-ttu-id="167e0-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="167e0-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="167e0-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="167e0-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="167e0-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="167e0-129">Continue</span></span>
- <span data-ttu-id="167e0-130">Över</span><span class="sxs-lookup"><span data-stu-id="167e0-130">Ignore</span></span>
- <span data-ttu-id="167e0-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="167e0-131">Inquire</span></span>
- <span data-ttu-id="167e0-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="167e0-132">SilentlyContinue</span></span>
- <span data-ttu-id="167e0-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="167e0-133">Stop</span></span>
- <span data-ttu-id="167e0-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="167e0-134">Suspend</span></span>

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

### <span data-ttu-id="167e0-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="167e0-135">-InformationVariable</span></span>
<span data-ttu-id="167e0-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="167e0-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="167e0-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="167e0-137">-InstanceName</span></span>
<span data-ttu-id="167e0-138">Anger namnet på den roll instans som ska återbildas eller startas om.</span><span class="sxs-lookup"><span data-stu-id="167e0-138">Specifies the name of the role instance to reimage or reboot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167e0-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="167e0-139">-Profile</span></span>
<span data-ttu-id="167e0-140">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="167e0-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="167e0-141">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="167e0-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="167e0-142">-Starta om</span><span class="sxs-lookup"><span data-stu-id="167e0-142">-Reboot</span></span>
<span data-ttu-id="167e0-143">Anger att den här cmdleten startar om den angivna roll instansen eller om ingen är angiven, alla roll instanser.</span><span class="sxs-lookup"><span data-stu-id="167e0-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="167e0-144">Du måste ange antingen en *omstart* eller en *bild* parameter, men inte båda.</span><span class="sxs-lookup"><span data-stu-id="167e0-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167e0-145">-Ombild</span><span class="sxs-lookup"><span data-stu-id="167e0-145">-Reimage</span></span>
<span data-ttu-id="167e0-146">Anger att denna cmdlet ombildar den angivna roll förekomsten eller, om ingen anges, alla roll instanser.</span><span class="sxs-lookup"><span data-stu-id="167e0-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="167e0-147">Du måste ange antingen en *omstart* eller en *bild* parameter, men inte båda.</span><span class="sxs-lookup"><span data-stu-id="167e0-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167e0-148">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="167e0-148">-ServiceName</span></span>
<span data-ttu-id="167e0-149">Anger namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="167e0-149">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="167e0-150">-Plats</span><span class="sxs-lookup"><span data-stu-id="167e0-150">-Slot</span></span>
<span data-ttu-id="167e0-151">Anger distributions miljön där roll instanserna körs.</span><span class="sxs-lookup"><span data-stu-id="167e0-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="167e0-152">Giltiga värden är: produktion och mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="167e0-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="167e0-153">Du kan inkludera antingen parametern *DeploymentName* eller *slot* , men inte båda.</span><span class="sxs-lookup"><span data-stu-id="167e0-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167e0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167e0-154">CommonParameters</span></span>
<span data-ttu-id="167e0-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="167e0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167e0-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="167e0-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167e0-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="167e0-157">INPUTS</span></span>

## <span data-ttu-id="167e0-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="167e0-158">OUTPUTS</span></span>

## <span data-ttu-id="167e0-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="167e0-159">NOTES</span></span>

## <span data-ttu-id="167e0-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="167e0-160">RELATED LINKS</span></span>

[<span data-ttu-id="167e0-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="167e0-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


