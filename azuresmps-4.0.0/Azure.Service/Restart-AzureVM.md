---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099303"
---
# <span data-ttu-id="16b60-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="16b60-101">Restart-AzureVM</span></span>

## <span data-ttu-id="16b60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16b60-102">SYNOPSIS</span></span>
<span data-ttu-id="16b60-103">Startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="16b60-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="16b60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16b60-104">SYNTAX</span></span>

### <span data-ttu-id="16b60-105">RestartByName (standard)</span><span class="sxs-lookup"><span data-stu-id="16b60-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="16b60-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="16b60-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="16b60-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="16b60-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="16b60-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="16b60-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="16b60-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="16b60-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="16b60-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="16b60-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="16b60-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16b60-111">DESCRIPTION</span></span>
<span data-ttu-id="16b60-112">Cmdleten **restart-AzureVM** begär en omstart av en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="16b60-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="16b60-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16b60-113">EXAMPLES</span></span>

### <span data-ttu-id="16b60-114">Exempel 1: starta om en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="16b60-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="16b60-115">Det här kommandot startar om den virtuella VirtualMachine27-datorn som körs i Azure-tjänsten med namnet Service01.</span><span class="sxs-lookup"><span data-stu-id="16b60-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="16b60-116">Exempel 2: starta om en virtuell dator med hjälp av ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="16b60-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="16b60-117">Det här kommandot hämtar det virtuella datorobjektet för den virtuella datorn med namnet MyVM och startar sedan om det.</span><span class="sxs-lookup"><span data-stu-id="16b60-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="16b60-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16b60-118">PARAMETERS</span></span>

### <span data-ttu-id="16b60-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="16b60-119">-InformationAction</span></span>
<span data-ttu-id="16b60-120">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="16b60-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="16b60-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="16b60-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16b60-122">Vidare</span><span class="sxs-lookup"><span data-stu-id="16b60-122">Continue</span></span>
- <span data-ttu-id="16b60-123">Över</span><span class="sxs-lookup"><span data-stu-id="16b60-123">Ignore</span></span>
- <span data-ttu-id="16b60-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="16b60-124">Inquire</span></span>
- <span data-ttu-id="16b60-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="16b60-125">SilentlyContinue</span></span>
- <span data-ttu-id="16b60-126">Stanna</span><span class="sxs-lookup"><span data-stu-id="16b60-126">Stop</span></span>
- <span data-ttu-id="16b60-127">Avbryt</span><span class="sxs-lookup"><span data-stu-id="16b60-127">Suspend</span></span>

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

### <span data-ttu-id="16b60-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="16b60-128">-InformationVariable</span></span>
<span data-ttu-id="16b60-129">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="16b60-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="16b60-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="16b60-130">-InitiateMaintenance</span></span>
<span data-ttu-id="16b60-131">Initiera underhåll på den virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="16b60-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b60-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="16b60-132">-Name</span></span>
<span data-ttu-id="16b60-133">Anger namnet på den virtuella datorn som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="16b60-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16b60-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="16b60-134">-Profile</span></span>
<span data-ttu-id="16b60-135">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="16b60-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16b60-136">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="16b60-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16b60-137">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="16b60-137">-Redeploy</span></span>
<span data-ttu-id="16b60-138">Anger att cmdleten distribuerar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="16b60-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b60-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="16b60-139">-ServiceName</span></span>
<span data-ttu-id="16b60-140">Anger namnet på den Azure-tjänst som innehåller den virtuella datorn som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="16b60-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="16b60-141">-VM</span><span class="sxs-lookup"><span data-stu-id="16b60-141">-VM</span></span>
<span data-ttu-id="16b60-142">Anger ett objekt för en virtuell dator som anger vilken virtuell dator som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="16b60-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16b60-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b60-143">CommonParameters</span></span>
<span data-ttu-id="16b60-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b60-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b60-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16b60-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b60-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16b60-146">INPUTS</span></span>

## <span data-ttu-id="16b60-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16b60-147">OUTPUTS</span></span>

## <span data-ttu-id="16b60-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16b60-148">NOTES</span></span>

## <span data-ttu-id="16b60-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16b60-149">RELATED LINKS</span></span>

[<span data-ttu-id="16b60-150">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="16b60-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="16b60-151">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="16b60-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="16b60-152">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="16b60-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="16b60-153">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="16b60-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="16b60-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="16b60-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


