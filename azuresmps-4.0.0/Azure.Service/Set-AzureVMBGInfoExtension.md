---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099273"
---
# <span data-ttu-id="06d4b-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="06d4b-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="06d4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="06d4b-103">Anger BGInfo-tillägget för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="06d4b-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="06d4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06d4b-104">SYNTAX</span></span>

### <span data-ttu-id="06d4b-105">SetBGInfoExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="06d4b-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="06d4b-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="06d4b-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="06d4b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06d4b-107">DESCRIPTION</span></span>
<span data-ttu-id="06d4b-108">Cmdleten **set-AzureVMBGInfoExtension** anger BgInfo-tillägget för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="06d4b-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="06d4b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06d4b-109">EXAMPLES</span></span>

### <span data-ttu-id="06d4b-110">Exempel 1: Ange BGInfo-tillägget för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="06d4b-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="06d4b-111">Det här kommandot anger BGInfo-tillägget för den angivna virtuella datorn enligt variabel $VM.</span><span class="sxs-lookup"><span data-stu-id="06d4b-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="06d4b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06d4b-112">PARAMETERS</span></span>

### <span data-ttu-id="06d4b-113">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="06d4b-113">-Disable</span></span>
<span data-ttu-id="06d4b-114">Anger att denna cmdlet inaktiverar tillägget.</span><span class="sxs-lookup"><span data-stu-id="06d4b-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d4b-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="06d4b-115">-InformationAction</span></span>
<span data-ttu-id="06d4b-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="06d4b-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06d4b-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="06d4b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06d4b-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="06d4b-118">Continue</span></span>
- <span data-ttu-id="06d4b-119">Över</span><span class="sxs-lookup"><span data-stu-id="06d4b-119">Ignore</span></span>
- <span data-ttu-id="06d4b-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="06d4b-120">Inquire</span></span>
- <span data-ttu-id="06d4b-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="06d4b-121">SilentlyContinue</span></span>
- <span data-ttu-id="06d4b-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="06d4b-122">Stop</span></span>
- <span data-ttu-id="06d4b-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="06d4b-123">Suspend</span></span>

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

### <span data-ttu-id="06d4b-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="06d4b-124">-InformationVariable</span></span>
<span data-ttu-id="06d4b-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="06d4b-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="06d4b-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="06d4b-126">-Profile</span></span>
<span data-ttu-id="06d4b-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="06d4b-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06d4b-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="06d4b-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06d4b-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="06d4b-129">-ReferenceName</span></span>
<span data-ttu-id="06d4b-130">Anger referens namnet för BGInfo-tillägget.</span><span class="sxs-lookup"><span data-stu-id="06d4b-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="06d4b-131">Den här parametern är en användardefinierad sträng som kan användas för att referera till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="06d4b-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="06d4b-132">Det anges när tillägget läggs till på den virtuella datorn för första gången.</span><span class="sxs-lookup"><span data-stu-id="06d4b-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="06d4b-133">Du kan ange tidigare Använd referens namn när du uppdaterar tillägget.</span><span class="sxs-lookup"><span data-stu-id="06d4b-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d4b-134">-Avinstallera</span><span class="sxs-lookup"><span data-stu-id="06d4b-134">-Uninstall</span></span>
<span data-ttu-id="06d4b-135">Anger att denna cmdlet avinstallerar tillägget BGInfo.</span><span class="sxs-lookup"><span data-stu-id="06d4b-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d4b-136">-Version</span><span class="sxs-lookup"><span data-stu-id="06d4b-136">-Version</span></span>
<span data-ttu-id="06d4b-137">Anger versionen för BGInfo-tillägget.</span><span class="sxs-lookup"><span data-stu-id="06d4b-137">Specifies the version of the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d4b-138">-VM</span><span class="sxs-lookup"><span data-stu-id="06d4b-138">-VM</span></span>
<span data-ttu-id="06d4b-139">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="06d4b-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="06d4b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d4b-140">CommonParameters</span></span>
<span data-ttu-id="06d4b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d4b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d4b-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d4b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d4b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06d4b-143">INPUTS</span></span>

## <span data-ttu-id="06d4b-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06d4b-144">OUTPUTS</span></span>

## <span data-ttu-id="06d4b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06d4b-145">NOTES</span></span>

## <span data-ttu-id="06d4b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06d4b-146">RELATED LINKS</span></span>

[<span data-ttu-id="06d4b-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="06d4b-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="06d4b-148">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="06d4b-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


