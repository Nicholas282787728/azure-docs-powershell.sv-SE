---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AC28E79-0E3F-4AED-8BFE-8D1C4DCB7715
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd7ece4f8f414df7be6e2d38920f516119f4b82a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099756"
---
# <span data-ttu-id="fb6b3-101">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="fb6b3-101">Get-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="fb6b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6b3-103">Hämtar Puppet-tillägget som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-103">Gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fb6b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb6b3-104">SYNTAX</span></span>

```
Get-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fb6b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="fb6b3-106">Cmdleten **Get-AzureVMPuppetExtension** hämtar fil namns tillägget Puppet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-106">The **Get-AzureVMPuppetExtension** cmdlet gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fb6b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb6b3-107">EXAMPLES</span></span>

### <span data-ttu-id="fb6b3-108">Exempel 1: få tillägget Puppet installerat på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="fb6b3-108">Example 1: Get the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Get-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="fb6b3-109">Det här kommandot får Puppet-tillägget kopplat till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-109">This command gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fb6b3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb6b3-110">PARAMETERS</span></span>

### <span data-ttu-id="fb6b3-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fb6b3-111">-InformationAction</span></span>
<span data-ttu-id="fb6b3-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fb6b3-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fb6b3-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb6b3-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="fb6b3-114">Continue</span></span>
- <span data-ttu-id="fb6b3-115">Över</span><span class="sxs-lookup"><span data-stu-id="fb6b3-115">Ignore</span></span>
- <span data-ttu-id="fb6b3-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="fb6b3-116">Inquire</span></span>
- <span data-ttu-id="fb6b3-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fb6b3-117">SilentlyContinue</span></span>
- <span data-ttu-id="fb6b3-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="fb6b3-118">Stop</span></span>
- <span data-ttu-id="fb6b3-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="fb6b3-119">Suspend</span></span>

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

### <span data-ttu-id="fb6b3-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fb6b3-120">-InformationVariable</span></span>
<span data-ttu-id="fb6b3-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fb6b3-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="fb6b3-122">-Profile</span></span>
<span data-ttu-id="fb6b3-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb6b3-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb6b3-125">-VM</span><span class="sxs-lookup"><span data-stu-id="fb6b3-125">-VM</span></span>
<span data-ttu-id="fb6b3-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="fb6b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6b3-127">CommonParameters</span></span>
<span data-ttu-id="fb6b3-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb6b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6b3-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6b3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6b3-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb6b3-130">INPUTS</span></span>

## <span data-ttu-id="fb6b3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb6b3-131">OUTPUTS</span></span>

## <span data-ttu-id="fb6b3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb6b3-132">NOTES</span></span>

## <span data-ttu-id="fb6b3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb6b3-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb6b3-134">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="fb6b3-134">Remove-AzureVMPuppetExtension</span></span>](./Remove-AzureVMPuppetExtension.md)

[<span data-ttu-id="fb6b3-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="fb6b3-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


