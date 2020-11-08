---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093467"
---
# <span data-ttu-id="853f3-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="853f3-101">Stop-AzureVM</span></span>

## <span data-ttu-id="853f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="853f3-102">SYNOPSIS</span></span>
<span data-ttu-id="853f3-103">Stänger av en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="853f3-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="853f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="853f3-104">SYNTAX</span></span>

### <span data-ttu-id="853f3-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="853f3-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="853f3-106">Flöde</span><span class="sxs-lookup"><span data-stu-id="853f3-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="853f3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="853f3-107">DESCRIPTION</span></span>
<span data-ttu-id="853f3-108">Cmdleten **Stop-AzureVM** stänger en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="853f3-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="853f3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="853f3-109">EXAMPLES</span></span>

### <span data-ttu-id="853f3-110">Exempel 1: avsluta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="853f3-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="853f3-111">Det här kommandot stänger av en virtuell dator som den angivna tjänsten innehåller.</span><span class="sxs-lookup"><span data-stu-id="853f3-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="853f3-112">Exempel 2: avsluta en virtuell dator med hjälp av ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="853f3-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="853f3-113">Det här kommandot stänger av en virtuell dator som den angivna tjänsten innehåller, med hjälp av det virtuella dator objekt som returnerar **-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="853f3-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="853f3-114">Exempel 3: avsluta en virtuell dator och låta den virtuella datorn vara etablerad</span><span class="sxs-lookup"><span data-stu-id="853f3-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="853f3-115">Det här kommandot stänger av en virtuell dator som den angivna tjänsten innehåller och behåller den etablerad.</span><span class="sxs-lookup"><span data-stu-id="853f3-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="853f3-116">Exempel 4: avsluta en virtuell dator och Tillåt avtilldelning av den senaste VM i distributionen</span><span class="sxs-lookup"><span data-stu-id="853f3-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="853f3-117">Det här kommandot stänger av en virtuell dator som den angivna tjänsten innehåller och tillåter avtilldelning av den senaste virtuella datorn i distributionen.</span><span class="sxs-lookup"><span data-stu-id="853f3-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="853f3-118">Exempel 5: avsluta flera virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="853f3-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="853f3-119">Det här kommandot stänger av flera virtuella datorer som den angivna tjänsten innehåller.</span><span class="sxs-lookup"><span data-stu-id="853f3-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="853f3-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="853f3-120">PARAMETERS</span></span>

### <span data-ttu-id="853f3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="853f3-121">-Force</span></span>
<span data-ttu-id="853f3-122">Anger om avtilldelning av den senaste virtuella datorn ska tillåtas i en distribution.</span><span class="sxs-lookup"><span data-stu-id="853f3-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853f3-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="853f3-123">-InformationAction</span></span>
<span data-ttu-id="853f3-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="853f3-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="853f3-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="853f3-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="853f3-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="853f3-126">Continue</span></span>
- <span data-ttu-id="853f3-127">Över</span><span class="sxs-lookup"><span data-stu-id="853f3-127">Ignore</span></span>
- <span data-ttu-id="853f3-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="853f3-128">Inquire</span></span>
- <span data-ttu-id="853f3-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="853f3-129">SilentlyContinue</span></span>
- <span data-ttu-id="853f3-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="853f3-130">Stop</span></span>
- <span data-ttu-id="853f3-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="853f3-131">Suspend</span></span>

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

### <span data-ttu-id="853f3-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="853f3-132">-InformationVariable</span></span>
<span data-ttu-id="853f3-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="853f3-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="853f3-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="853f3-134">-Name</span></span>
<span data-ttu-id="853f3-135">Anger namnet på den virtuella datorn som ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="853f3-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="853f3-136">Använd jokertecknet för att stoppa flera virtuella datorer asynkront.</span><span class="sxs-lookup"><span data-stu-id="853f3-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="853f3-137">Med ett jokertecken anropar den här cmdlet åtgärden avsluta https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) i stället för rollen avsluta https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx åtgärd ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .</span><span class="sxs-lookup"><span data-stu-id="853f3-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="853f3-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="853f3-138">-Profile</span></span>
<span data-ttu-id="853f3-139">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="853f3-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="853f3-140">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="853f3-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="853f3-141">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="853f3-141">-ServiceName</span></span>
<span data-ttu-id="853f3-142">Anger namnet på den Azure-tjänst som innehåller den virtuella datorn som ska stängas av.</span><span class="sxs-lookup"><span data-stu-id="853f3-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="853f3-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="853f3-143">-StayProvisioned</span></span>
<span data-ttu-id="853f3-144">Anger att denna cmdlet håller den virtuella datorn etablerad.</span><span class="sxs-lookup"><span data-stu-id="853f3-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853f3-145">-VM</span><span class="sxs-lookup"><span data-stu-id="853f3-145">-VM</span></span>
<span data-ttu-id="853f3-146">Anger ett objekt för virtuell dator som identifierar den virtuella datorn för avstängning.</span><span class="sxs-lookup"><span data-stu-id="853f3-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="853f3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="853f3-147">CommonParameters</span></span>
<span data-ttu-id="853f3-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="853f3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="853f3-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="853f3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="853f3-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="853f3-150">INPUTS</span></span>

## <span data-ttu-id="853f3-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="853f3-151">OUTPUTS</span></span>

## <span data-ttu-id="853f3-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="853f3-152">NOTES</span></span>

## <span data-ttu-id="853f3-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="853f3-153">RELATED LINKS</span></span>

[<span data-ttu-id="853f3-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="853f3-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="853f3-155">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="853f3-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="853f3-156">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="853f3-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="853f3-157">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="853f3-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


