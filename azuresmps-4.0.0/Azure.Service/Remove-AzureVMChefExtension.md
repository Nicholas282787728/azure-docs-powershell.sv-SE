---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093231"
---
# <span data-ttu-id="dc5ad-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="dc5ad-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="dc5ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5ad-103">Tar bort den kock-anknytning som tillämpas på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="dc5ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc5ad-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dc5ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc5ad-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5ad-106">Cmdleten **Remove-AzureVMChefExtension** tar bort kock-tillägget som används på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="dc5ad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc5ad-107">EXAMPLES</span></span>

### <span data-ttu-id="dc5ad-108">Exempel 1: ta bort kock-tillägget som används på den angivna virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="dc5ad-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="dc5ad-109">Det här kommandot tar bort kock-tillägget som används på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="dc5ad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc5ad-110">PARAMETERS</span></span>

### <span data-ttu-id="dc5ad-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dc5ad-111">-InformationAction</span></span>
<span data-ttu-id="dc5ad-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dc5ad-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dc5ad-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dc5ad-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="dc5ad-114">Continue</span></span>
- <span data-ttu-id="dc5ad-115">Över</span><span class="sxs-lookup"><span data-stu-id="dc5ad-115">Ignore</span></span>
- <span data-ttu-id="dc5ad-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="dc5ad-116">Inquire</span></span>
- <span data-ttu-id="dc5ad-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dc5ad-117">SilentlyContinue</span></span>
- <span data-ttu-id="dc5ad-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="dc5ad-118">Stop</span></span>
- <span data-ttu-id="dc5ad-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="dc5ad-119">Suspend</span></span>

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

### <span data-ttu-id="dc5ad-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dc5ad-120">-InformationVariable</span></span>
<span data-ttu-id="dc5ad-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dc5ad-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="dc5ad-122">-Profile</span></span>
<span data-ttu-id="dc5ad-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc5ad-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc5ad-125">-VM</span><span class="sxs-lookup"><span data-stu-id="dc5ad-125">-VM</span></span>
<span data-ttu-id="dc5ad-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="dc5ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5ad-127">CommonParameters</span></span>
<span data-ttu-id="dc5ad-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5ad-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5ad-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc5ad-130">INPUTS</span></span>

## <span data-ttu-id="dc5ad-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc5ad-131">OUTPUTS</span></span>

## <span data-ttu-id="dc5ad-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc5ad-132">NOTES</span></span>

## <span data-ttu-id="dc5ad-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc5ad-133">RELATED LINKS</span></span>

[<span data-ttu-id="dc5ad-134">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="dc5ad-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="dc5ad-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="dc5ad-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


