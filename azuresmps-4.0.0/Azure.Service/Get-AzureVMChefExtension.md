---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099775"
---
# <span data-ttu-id="c7c20-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c7c20-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="c7c20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7c20-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c20-103">Får kock-tillägget installerat på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c7c20-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="c7c20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7c20-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c7c20-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7c20-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c20-106">Cmdleten **Get-AzureVMChefExtension** får kock-tillägget installerat på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c7c20-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="c7c20-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7c20-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c20-108">Exempel 1: Hämta det kock-tillägg som används på den angivna virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="c7c20-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="c7c20-109">Det här kommandot får kock-tillägget installerat på den angivna virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c7c20-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="c7c20-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7c20-110">PARAMETERS</span></span>

### <span data-ttu-id="c7c20-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c7c20-111">-InformationAction</span></span>
<span data-ttu-id="c7c20-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c7c20-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c7c20-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c7c20-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7c20-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="c7c20-114">Continue</span></span>
- <span data-ttu-id="c7c20-115">Över</span><span class="sxs-lookup"><span data-stu-id="c7c20-115">Ignore</span></span>
- <span data-ttu-id="c7c20-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="c7c20-116">Inquire</span></span>
- <span data-ttu-id="c7c20-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c7c20-117">SilentlyContinue</span></span>
- <span data-ttu-id="c7c20-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="c7c20-118">Stop</span></span>
- <span data-ttu-id="c7c20-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c7c20-119">Suspend</span></span>

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

### <span data-ttu-id="c7c20-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c7c20-120">-InformationVariable</span></span>
<span data-ttu-id="c7c20-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c7c20-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c7c20-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7c20-122">-Profile</span></span>
<span data-ttu-id="c7c20-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c7c20-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7c20-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c7c20-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7c20-125">-VM</span><span class="sxs-lookup"><span data-stu-id="c7c20-125">-VM</span></span>
<span data-ttu-id="c7c20-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="c7c20-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c7c20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c20-127">CommonParameters</span></span>
<span data-ttu-id="c7c20-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c20-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c20-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c20-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7c20-130">INPUTS</span></span>

## <span data-ttu-id="c7c20-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7c20-131">OUTPUTS</span></span>

## <span data-ttu-id="c7c20-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7c20-132">NOTES</span></span>

## <span data-ttu-id="c7c20-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7c20-133">RELATED LINKS</span></span>

[<span data-ttu-id="c7c20-134">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c7c20-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="c7c20-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c7c20-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


