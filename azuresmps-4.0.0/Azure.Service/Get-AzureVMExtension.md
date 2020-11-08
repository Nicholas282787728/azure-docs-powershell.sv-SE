---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099763"
---
# <span data-ttu-id="c6abb-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c6abb-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="c6abb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6abb-102">SYNOPSIS</span></span>
<span data-ttu-id="c6abb-103">Hämtar resurs tillägg på virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="c6abb-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="c6abb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6abb-104">SYNTAX</span></span>

### <span data-ttu-id="c6abb-105">ListByReferenceName (standard)</span><span class="sxs-lookup"><span data-stu-id="c6abb-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c6abb-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="c6abb-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6abb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6abb-107">DESCRIPTION</span></span>
<span data-ttu-id="c6abb-108">Cmdleten **Get-AzureVMExtension** hämtar resurs tillägg som tillämpas på virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="c6abb-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="c6abb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6abb-109">EXAMPLES</span></span>

### <span data-ttu-id="c6abb-110">Exempel 1: få resurs tilläggen kopplade till en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c6abb-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="c6abb-111">Det här kommandot får de resurs tillägg som tillämpas på den angivna virtuella datorn enligt variabel $VM.</span><span class="sxs-lookup"><span data-stu-id="c6abb-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="c6abb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6abb-112">PARAMETERS</span></span>

### <span data-ttu-id="c6abb-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c6abb-113">-ExtensionName</span></span>
<span data-ttu-id="c6abb-114">Anger tillägget för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c6abb-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6abb-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c6abb-115">-InformationAction</span></span>
<span data-ttu-id="c6abb-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c6abb-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c6abb-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c6abb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6abb-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="c6abb-118">Continue</span></span>
- <span data-ttu-id="c6abb-119">Över</span><span class="sxs-lookup"><span data-stu-id="c6abb-119">Ignore</span></span>
- <span data-ttu-id="c6abb-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="c6abb-120">Inquire</span></span>
- <span data-ttu-id="c6abb-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c6abb-121">SilentlyContinue</span></span>
- <span data-ttu-id="c6abb-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="c6abb-122">Stop</span></span>
- <span data-ttu-id="c6abb-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c6abb-123">Suspend</span></span>

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

### <span data-ttu-id="c6abb-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c6abb-124">-InformationVariable</span></span>
<span data-ttu-id="c6abb-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c6abb-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c6abb-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="c6abb-126">-Profile</span></span>
<span data-ttu-id="c6abb-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c6abb-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6abb-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c6abb-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6abb-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c6abb-129">-Publisher</span></span>
<span data-ttu-id="c6abb-130">Anger utgivaren av tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6abb-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6abb-131">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="c6abb-131">-ReferenceName</span></span>
<span data-ttu-id="c6abb-132">Anger anknytningens referens namn.</span><span class="sxs-lookup"><span data-stu-id="c6abb-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6abb-133">-Version</span><span class="sxs-lookup"><span data-stu-id="c6abb-133">-Version</span></span>
<span data-ttu-id="c6abb-134">Anger version för tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6abb-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6abb-135">-VM</span><span class="sxs-lookup"><span data-stu-id="c6abb-135">-VM</span></span>
<span data-ttu-id="c6abb-136">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="c6abb-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c6abb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6abb-137">CommonParameters</span></span>
<span data-ttu-id="c6abb-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6abb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6abb-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6abb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6abb-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6abb-140">INPUTS</span></span>

## <span data-ttu-id="c6abb-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6abb-141">OUTPUTS</span></span>

## <span data-ttu-id="c6abb-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6abb-142">NOTES</span></span>

## <span data-ttu-id="c6abb-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6abb-143">RELATED LINKS</span></span>

[<span data-ttu-id="c6abb-144">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c6abb-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="c6abb-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c6abb-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


