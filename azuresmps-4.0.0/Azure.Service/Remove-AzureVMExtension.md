---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093227"
---
# <span data-ttu-id="e3703-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="e3703-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="e3703-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3703-102">SYNOPSIS</span></span>
<span data-ttu-id="e3703-103">Tar bort resurs tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e3703-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="e3703-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3703-104">SYNTAX</span></span>

### <span data-ttu-id="e3703-105">RemoveByExtensionName (standard)</span><span class="sxs-lookup"><span data-stu-id="e3703-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3703-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="e3703-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e3703-107">RemoveAll</span><span class="sxs-lookup"><span data-stu-id="e3703-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e3703-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3703-108">DESCRIPTION</span></span>
<span data-ttu-id="e3703-109">Cmdleten **Remove-AzureVMExtension** tar bort resurs tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e3703-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="e3703-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3703-110">EXAMPLES</span></span>

### <span data-ttu-id="e3703-111">Exempel 1: ta bort ett tillägg med ett specifikt namn och Publisher</span><span class="sxs-lookup"><span data-stu-id="e3703-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="e3703-112">Det här kommandot tar bort ett tillägg med angivet namn och utgivare.</span><span class="sxs-lookup"><span data-stu-id="e3703-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="e3703-113">Exempel 2: ta bort alla tillägg från en specifik virtuell dator</span><span class="sxs-lookup"><span data-stu-id="e3703-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="e3703-114">Det här kommandot tar bort alla tillägg från den angivna virtuella datorn enligt variabel $VM.</span><span class="sxs-lookup"><span data-stu-id="e3703-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="e3703-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3703-115">PARAMETERS</span></span>

### <span data-ttu-id="e3703-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e3703-116">-ExtensionName</span></span>
<span data-ttu-id="e3703-117">Anger det tilläggs namn som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e3703-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3703-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e3703-118">-InformationAction</span></span>
<span data-ttu-id="e3703-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e3703-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e3703-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e3703-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3703-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="e3703-121">Continue</span></span>
- <span data-ttu-id="e3703-122">Över</span><span class="sxs-lookup"><span data-stu-id="e3703-122">Ignore</span></span>
- <span data-ttu-id="e3703-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="e3703-123">Inquire</span></span>
- <span data-ttu-id="e3703-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e3703-124">SilentlyContinue</span></span>
- <span data-ttu-id="e3703-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="e3703-125">Stop</span></span>
- <span data-ttu-id="e3703-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e3703-126">Suspend</span></span>

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

### <span data-ttu-id="e3703-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e3703-127">-InformationVariable</span></span>
<span data-ttu-id="e3703-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e3703-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e3703-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="e3703-129">-Profile</span></span>
<span data-ttu-id="e3703-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e3703-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3703-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e3703-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3703-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e3703-132">-Publisher</span></span>
<span data-ttu-id="e3703-133">Anger anknytnings utgivaren.</span><span class="sxs-lookup"><span data-stu-id="e3703-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3703-134">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="e3703-134">-ReferenceName</span></span>
<span data-ttu-id="e3703-135">Anger anknytningens referens namn.</span><span class="sxs-lookup"><span data-stu-id="e3703-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3703-136">-RemoveAll</span><span class="sxs-lookup"><span data-stu-id="e3703-136">-RemoveAll</span></span>
<span data-ttu-id="e3703-137">Anger att denna cmdlet tar bort alla resurs tillägg från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e3703-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3703-138">-VM</span><span class="sxs-lookup"><span data-stu-id="e3703-138">-VM</span></span>
<span data-ttu-id="e3703-139">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="e3703-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="e3703-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3703-140">CommonParameters</span></span>
<span data-ttu-id="e3703-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3703-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3703-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3703-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3703-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3703-143">INPUTS</span></span>

## <span data-ttu-id="e3703-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3703-144">OUTPUTS</span></span>

## <span data-ttu-id="e3703-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3703-145">NOTES</span></span>

## <span data-ttu-id="e3703-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3703-146">RELATED LINKS</span></span>

[<span data-ttu-id="e3703-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="e3703-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="e3703-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="e3703-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


