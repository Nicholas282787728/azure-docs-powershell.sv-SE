---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099001"
---
# <span data-ttu-id="e6273-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6273-101">Start-AzureVM</span></span>

## <span data-ttu-id="e6273-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6273-102">SYNOPSIS</span></span>
<span data-ttu-id="e6273-103">Startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="e6273-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="e6273-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6273-104">SYNTAX</span></span>

### <span data-ttu-id="e6273-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="e6273-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e6273-106">Flöde</span><span class="sxs-lookup"><span data-stu-id="e6273-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e6273-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6273-107">DESCRIPTION</span></span>
<span data-ttu-id="e6273-108">Cmdleten **Start-AzureVM** startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="e6273-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="e6273-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6273-109">EXAMPLES</span></span>

### <span data-ttu-id="e6273-110">Exempel 1: starta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="e6273-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="e6273-111">Det här kommandot startar den virtuella datorn med namnet VirtualMachine04 som körs i Azure-tjänsten med namnet ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="e6273-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="e6273-112">Exempel 2: starta en virtuell dator med ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="e6273-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="e6273-113">Det här kommandot hämtar det virtuella datorobjektet för den virtuella datorn vars namn är DatabaseServer och begär sedan att starta det.</span><span class="sxs-lookup"><span data-stu-id="e6273-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="e6273-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6273-114">PARAMETERS</span></span>

### <span data-ttu-id="e6273-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e6273-115">-InformationAction</span></span>
<span data-ttu-id="e6273-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e6273-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e6273-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e6273-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6273-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="e6273-118">Continue</span></span>
- <span data-ttu-id="e6273-119">Över</span><span class="sxs-lookup"><span data-stu-id="e6273-119">Ignore</span></span>
- <span data-ttu-id="e6273-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="e6273-120">Inquire</span></span>
- <span data-ttu-id="e6273-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e6273-121">SilentlyContinue</span></span>
- <span data-ttu-id="e6273-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="e6273-122">Stop</span></span>
- <span data-ttu-id="e6273-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e6273-123">Suspend</span></span>

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

### <span data-ttu-id="e6273-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e6273-124">-InformationVariable</span></span>
<span data-ttu-id="e6273-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e6273-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e6273-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6273-126">-Name</span></span>
<span data-ttu-id="e6273-127">Anger namnet på den virtuella dator som ska startas.</span><span class="sxs-lookup"><span data-stu-id="e6273-127">Specifies the name of the virtual machine to start.</span></span>

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

### <span data-ttu-id="e6273-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="e6273-128">-Profile</span></span>
<span data-ttu-id="e6273-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e6273-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6273-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e6273-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6273-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e6273-131">-ServiceName</span></span>
<span data-ttu-id="e6273-132">Anger namnet på den Azure-tjänst som innehåller den virtuella datorn som ska startas.</span><span class="sxs-lookup"><span data-stu-id="e6273-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

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

### <span data-ttu-id="e6273-133">-VM</span><span class="sxs-lookup"><span data-stu-id="e6273-133">-VM</span></span>
<span data-ttu-id="e6273-134">Anger ett objekt för en virtuell dator som anger vilken virtuell dator som ska startas.</span><span class="sxs-lookup"><span data-stu-id="e6273-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

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

### <span data-ttu-id="e6273-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6273-135">CommonParameters</span></span>
<span data-ttu-id="e6273-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6273-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6273-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6273-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6273-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6273-138">INPUTS</span></span>

## <span data-ttu-id="e6273-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6273-139">OUTPUTS</span></span>

## <span data-ttu-id="e6273-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6273-140">NOTES</span></span>

## <span data-ttu-id="e6273-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6273-141">RELATED LINKS</span></span>

[<span data-ttu-id="e6273-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6273-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="e6273-143">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6273-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="e6273-144">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6273-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="e6273-145">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6273-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="e6273-146">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6273-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


