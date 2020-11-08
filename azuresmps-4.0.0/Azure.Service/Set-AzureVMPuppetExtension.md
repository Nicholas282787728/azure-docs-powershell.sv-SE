---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099079"
---
# <span data-ttu-id="aaa38-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="aaa38-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="aaa38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aaa38-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa38-103">Anger Puppet-tillägget för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aaa38-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="aaa38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aaa38-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aaa38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aaa38-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa38-106">Cmdleten **set-AzureVMPuppetExtension** anger Puppet-tillägget för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aaa38-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="aaa38-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aaa38-107">EXAMPLES</span></span>

### <span data-ttu-id="aaa38-108">Exempel 1: Ange Puppet-tillägget för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="aaa38-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="aaa38-109">I det här exemplet anges Puppet-tillägget för den angivna virtuella datorn enligt variabel $VM.</span><span class="sxs-lookup"><span data-stu-id="aaa38-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="aaa38-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aaa38-110">PARAMETERS</span></span>

### <span data-ttu-id="aaa38-111">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="aaa38-111">-Disable</span></span>
<span data-ttu-id="aaa38-112">Anger att denna cmdlet inaktiverar tillägget.</span><span class="sxs-lookup"><span data-stu-id="aaa38-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa38-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aaa38-113">-InformationAction</span></span>
<span data-ttu-id="aaa38-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="aaa38-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aaa38-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aaa38-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aaa38-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="aaa38-116">Continue</span></span>
- <span data-ttu-id="aaa38-117">Över</span><span class="sxs-lookup"><span data-stu-id="aaa38-117">Ignore</span></span>
- <span data-ttu-id="aaa38-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="aaa38-118">Inquire</span></span>
- <span data-ttu-id="aaa38-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aaa38-119">SilentlyContinue</span></span>
- <span data-ttu-id="aaa38-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="aaa38-120">Stop</span></span>
- <span data-ttu-id="aaa38-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="aaa38-121">Suspend</span></span>

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

### <span data-ttu-id="aaa38-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aaa38-122">-InformationVariable</span></span>
<span data-ttu-id="aaa38-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="aaa38-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aaa38-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="aaa38-124">-Profile</span></span>
<span data-ttu-id="aaa38-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="aaa38-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aaa38-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="aaa38-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aaa38-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="aaa38-127">-PuppetMasterServer</span></span>
<span data-ttu-id="aaa38-128">Anger det fullständigt kvalificerade domän namnet (FQDN) för Puppet Master server.</span><span class="sxs-lookup"><span data-stu-id="aaa38-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

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

### <span data-ttu-id="aaa38-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="aaa38-129">-ReferenceName</span></span>
<span data-ttu-id="aaa38-130">Anger anknytningens referens namn.</span><span class="sxs-lookup"><span data-stu-id="aaa38-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="aaa38-131">Det här är en användardefinierad sträng som används för att referera till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="aaa38-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="aaa38-132">Det anges när tillägget läggs till på den virtuella datorn för första gången.</span><span class="sxs-lookup"><span data-stu-id="aaa38-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="aaa38-133">För kommande uppdateringar måste du ange det referens namn som används tidigare när du uppdaterar tillägget.</span><span class="sxs-lookup"><span data-stu-id="aaa38-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="aaa38-134">ReferenceName som tilldelats till ett tillägg returneras med cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="aaa38-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa38-135">-Version</span><span class="sxs-lookup"><span data-stu-id="aaa38-135">-Version</span></span>
<span data-ttu-id="aaa38-136">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="aaa38-136">Specifies the extension version.</span></span>

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

### <span data-ttu-id="aaa38-137">-VM</span><span class="sxs-lookup"><span data-stu-id="aaa38-137">-VM</span></span>
<span data-ttu-id="aaa38-138">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="aaa38-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="aaa38-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa38-139">CommonParameters</span></span>
<span data-ttu-id="aaa38-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa38-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa38-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa38-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa38-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aaa38-142">INPUTS</span></span>

## <span data-ttu-id="aaa38-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aaa38-143">OUTPUTS</span></span>

## <span data-ttu-id="aaa38-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aaa38-144">NOTES</span></span>

## <span data-ttu-id="aaa38-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aaa38-145">RELATED LINKS</span></span>

[<span data-ttu-id="aaa38-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aaa38-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


