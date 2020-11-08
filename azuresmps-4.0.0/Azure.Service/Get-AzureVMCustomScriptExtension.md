---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093257"
---
# <span data-ttu-id="1e1cc-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1e1cc-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="1e1cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1cc-103">Hämtar information från ett anpassat skript tillägg för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="1e1cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e1cc-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e1cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e1cc-105">DESCRIPTION</span></span>
<span data-ttu-id="1e1cc-106">Cmdleten **Get-AzureVMCustomScriptExtension** hämtar information från ett anpassat skript tillägg för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="1e1cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e1cc-107">EXAMPLES</span></span>

### <span data-ttu-id="1e1cc-108">Exempel 1: Hämta ett skript tillägg för en Azure Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="1e1cc-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="1e1cc-109">Det här kommandot får ett skript tillägg för Azure Virtual Machine lagrat i variabeln $VM.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="1e1cc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e1cc-110">PARAMETERS</span></span>

### <span data-ttu-id="1e1cc-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1e1cc-111">-InformationAction</span></span>
<span data-ttu-id="1e1cc-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e1cc-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1e1cc-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e1cc-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="1e1cc-114">Continue</span></span>
- <span data-ttu-id="1e1cc-115">Över</span><span class="sxs-lookup"><span data-stu-id="1e1cc-115">Ignore</span></span>
- <span data-ttu-id="1e1cc-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="1e1cc-116">Inquire</span></span>
- <span data-ttu-id="1e1cc-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e1cc-117">SilentlyContinue</span></span>
- <span data-ttu-id="1e1cc-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="1e1cc-118">Stop</span></span>
- <span data-ttu-id="1e1cc-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="1e1cc-119">Suspend</span></span>

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

### <span data-ttu-id="1e1cc-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e1cc-120">-InformationVariable</span></span>
<span data-ttu-id="1e1cc-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1e1cc-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e1cc-122">-Profile</span></span>
<span data-ttu-id="1e1cc-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e1cc-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e1cc-125">-VM</span><span class="sxs-lookup"><span data-stu-id="1e1cc-125">-VM</span></span>
<span data-ttu-id="1e1cc-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="1e1cc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1cc-127">CommonParameters</span></span>
<span data-ttu-id="1e1cc-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e1cc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1cc-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e1cc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1cc-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e1cc-130">INPUTS</span></span>

## <span data-ttu-id="1e1cc-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e1cc-131">OUTPUTS</span></span>

## <span data-ttu-id="1e1cc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e1cc-132">NOTES</span></span>

## <span data-ttu-id="1e1cc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e1cc-133">RELATED LINKS</span></span>

[<span data-ttu-id="1e1cc-134">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1e1cc-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="1e1cc-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1e1cc-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


