---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AAEDD44-D11E-47A3-BF0F-D8445A018759
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46dbd7ec58cc112e6573fa3d9c6a52fe0ee14b33
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099673"
---
# <span data-ttu-id="cd833-101">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="cd833-101">Remove-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="cd833-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd833-102">SYNOPSIS</span></span>
<span data-ttu-id="cd833-103">Tar bort tillägget Puppet som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cd833-103">Removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="cd833-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd833-104">SYNTAX</span></span>

```
Remove-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cd833-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd833-105">DESCRIPTION</span></span>
<span data-ttu-id="cd833-106">Cmdleten **Remove-AzureVMPuppetExtension** tar bort tillägget Puppet som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cd833-106">The **Remove-AzureVMPuppetExtension** cmdlet removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="cd833-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd833-107">EXAMPLES</span></span>

### <span data-ttu-id="cd833-108">Exempel 1: ta bort Puppet-tillägget som används på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="cd833-108">Example 1: Remove the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMPuppetExtension -VM $VM;
```

<span data-ttu-id="cd833-109">Det här kommandot tar bort tillägget Puppet som används på den angivna virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cd833-109">This command removes the Puppet extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="cd833-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd833-110">PARAMETERS</span></span>

### <span data-ttu-id="cd833-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cd833-111">-InformationAction</span></span>
<span data-ttu-id="cd833-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="cd833-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cd833-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cd833-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd833-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="cd833-114">Continue</span></span>
- <span data-ttu-id="cd833-115">Över</span><span class="sxs-lookup"><span data-stu-id="cd833-115">Ignore</span></span>
- <span data-ttu-id="cd833-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="cd833-116">Inquire</span></span>
- <span data-ttu-id="cd833-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cd833-117">SilentlyContinue</span></span>
- <span data-ttu-id="cd833-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="cd833-118">Stop</span></span>
- <span data-ttu-id="cd833-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="cd833-119">Suspend</span></span>

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

### <span data-ttu-id="cd833-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cd833-120">-InformationVariable</span></span>
<span data-ttu-id="cd833-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="cd833-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cd833-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="cd833-122">-Profile</span></span>
<span data-ttu-id="cd833-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="cd833-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd833-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="cd833-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd833-125">-VM</span><span class="sxs-lookup"><span data-stu-id="cd833-125">-VM</span></span>
<span data-ttu-id="cd833-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="cd833-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="cd833-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd833-127">CommonParameters</span></span>
<span data-ttu-id="cd833-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd833-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd833-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd833-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd833-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd833-130">INPUTS</span></span>

## <span data-ttu-id="cd833-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd833-131">OUTPUTS</span></span>

## <span data-ttu-id="cd833-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd833-132">NOTES</span></span>

## <span data-ttu-id="cd833-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd833-133">RELATED LINKS</span></span>

[<span data-ttu-id="cd833-134">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="cd833-134">Get-AzureVMPuppetExtension</span></span>](./Get-AzureVMPuppetExtension.md)

[<span data-ttu-id="cd833-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="cd833-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


