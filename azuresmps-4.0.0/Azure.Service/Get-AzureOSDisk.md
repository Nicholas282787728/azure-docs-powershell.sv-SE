---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099562"
---
# <span data-ttu-id="7d344-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="7d344-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="7d344-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d344-102">SYNOPSIS</span></span>
<span data-ttu-id="7d344-103">Hämtar operativ system disken för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="7d344-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="7d344-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d344-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7d344-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d344-105">DESCRIPTION</span></span>
<span data-ttu-id="7d344-106">Cmdleten **Get-AzureOSDisk** hämtar operativ system disken för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="7d344-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="7d344-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d344-107">EXAMPLES</span></span>

### <span data-ttu-id="7d344-108">Exempel 1: skaffa en operativ Systems diskett</span><span class="sxs-lookup"><span data-stu-id="7d344-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="7d344-109">Det här kommandot får den virtuella datorn som heter VirtualMachine02 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="7d344-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="7d344-110">Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="7d344-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7d344-111">Den aktuella cmdleten får operativ system disken på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7d344-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="7d344-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d344-112">PARAMETERS</span></span>

### <span data-ttu-id="7d344-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7d344-113">-InformationAction</span></span>
<span data-ttu-id="7d344-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="7d344-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7d344-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7d344-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d344-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="7d344-116">Continue</span></span>
- <span data-ttu-id="7d344-117">Över</span><span class="sxs-lookup"><span data-stu-id="7d344-117">Ignore</span></span>
- <span data-ttu-id="7d344-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="7d344-118">Inquire</span></span>
- <span data-ttu-id="7d344-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7d344-119">SilentlyContinue</span></span>
- <span data-ttu-id="7d344-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="7d344-120">Stop</span></span>
- <span data-ttu-id="7d344-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="7d344-121">Suspend</span></span>

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

### <span data-ttu-id="7d344-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7d344-122">-InformationVariable</span></span>
<span data-ttu-id="7d344-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="7d344-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7d344-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="7d344-124">-Profile</span></span>
<span data-ttu-id="7d344-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7d344-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d344-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7d344-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d344-127">-VM</span><span class="sxs-lookup"><span data-stu-id="7d344-127">-VM</span></span>
<span data-ttu-id="7d344-128">Anger den virtuella dator för vilken denna cmdlet får operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="7d344-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="7d344-129">Använd cmdleten **Get-AzureVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="7d344-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="7d344-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d344-130">CommonParameters</span></span>
<span data-ttu-id="7d344-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d344-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d344-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d344-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d344-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d344-133">INPUTS</span></span>

## <span data-ttu-id="7d344-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d344-134">OUTPUTS</span></span>

## <span data-ttu-id="7d344-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d344-135">NOTES</span></span>

## <span data-ttu-id="7d344-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d344-136">RELATED LINKS</span></span>

[<span data-ttu-id="7d344-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="7d344-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="7d344-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="7d344-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


