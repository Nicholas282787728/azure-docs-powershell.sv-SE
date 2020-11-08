---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099021"
---
# <span data-ttu-id="c4740-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="c4740-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="c4740-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4740-102">SYNOPSIS</span></span>
<span data-ttu-id="c4740-103">Anger storleken på en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="c4740-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="c4740-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4740-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c4740-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4740-105">DESCRIPTION</span></span>
<span data-ttu-id="c4740-106">Cmdleten **set-AzureVMSize** uppdaterar storleken på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c4740-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="c4740-107">Den har två parametrar: *InstanceSize* , som är den nya storleken på den virtuella datorn och *VM* , vilket är ett virtuellt dator-objekt som hämtas med cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="c4740-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c4740-108">Resultatet från **set-AzureVMSize** kan vara piped till cmdleten **Update-AzureVM** eller lagras i en variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="c4740-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="c4740-109">Ingen verklig ändring görs förrän **Update-AzureVM** körs.</span><span class="sxs-lookup"><span data-stu-id="c4740-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="c4740-110">OBS! den här cmdleten kräver att den virtuella datorn reserveras och den kan ha en ny IP-adress.</span><span class="sxs-lookup"><span data-stu-id="c4740-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="c4740-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4740-111">EXAMPLES</span></span>

### <span data-ttu-id="c4740-112">Exempel 1: Ange storleken på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c4740-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="c4740-113">Det här kommandot uppdaterar en virtuell dator för att ändra storlek "liten".</span><span class="sxs-lookup"><span data-stu-id="c4740-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="c4740-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4740-114">PARAMETERS</span></span>

### <span data-ttu-id="c4740-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c4740-115">-InformationAction</span></span>
<span data-ttu-id="c4740-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c4740-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c4740-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c4740-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4740-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="c4740-118">Continue</span></span>
- <span data-ttu-id="c4740-119">Över</span><span class="sxs-lookup"><span data-stu-id="c4740-119">Ignore</span></span>
- <span data-ttu-id="c4740-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="c4740-120">Inquire</span></span>
- <span data-ttu-id="c4740-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c4740-121">SilentlyContinue</span></span>
- <span data-ttu-id="c4740-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="c4740-122">Stop</span></span>
- <span data-ttu-id="c4740-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c4740-123">Suspend</span></span>

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

### <span data-ttu-id="c4740-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c4740-124">-InformationVariable</span></span>
<span data-ttu-id="c4740-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c4740-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c4740-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="c4740-126">-InstanceSize</span></span>
<span data-ttu-id="c4740-127">Anger storleken på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c4740-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="c4740-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c4740-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="c4740-129">--ExtraSmall--Small--Large--Large--ExtraLarge--A5--A6--A7</span><span class="sxs-lookup"><span data-stu-id="c4740-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

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

### <span data-ttu-id="c4740-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4740-130">-Profile</span></span>
<span data-ttu-id="c4740-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c4740-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4740-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c4740-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4740-133">-VM</span><span class="sxs-lookup"><span data-stu-id="c4740-133">-VM</span></span>
<span data-ttu-id="c4740-134">Anger det beständiga virtuella dator objekt som denna cmdlet ställer in storleken på.</span><span class="sxs-lookup"><span data-stu-id="c4740-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4740-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4740-135">CommonParameters</span></span>
<span data-ttu-id="c4740-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4740-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4740-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4740-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4740-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4740-138">INPUTS</span></span>

## <span data-ttu-id="c4740-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4740-139">OUTPUTS</span></span>

## <span data-ttu-id="c4740-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4740-140">NOTES</span></span>

## <span data-ttu-id="c4740-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4740-141">RELATED LINKS</span></span>

[<span data-ttu-id="c4740-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c4740-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c4740-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c4740-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


