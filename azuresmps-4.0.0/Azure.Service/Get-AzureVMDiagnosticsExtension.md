---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E1A3FF-E479-44CD-8147-15408DF3F79A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f8290b0e4f40305495b535b28b2a8f61d7911ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099773"
---
# <span data-ttu-id="f5509-101">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f5509-101">Get-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="f5509-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5509-102">SYNOPSIS</span></span>
<span data-ttu-id="f5509-103">Hämtar inställningar för Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f5509-103">Gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="f5509-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5509-104">SYNTAX</span></span>

```
Get-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f5509-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5509-105">DESCRIPTION</span></span>
<span data-ttu-id="f5509-106">Cmdleten **Get-AzureVMDiagnosticsExtension** hämtar inställningarna för Microsoft Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f5509-106">The **Get-AzureVMDiagnosticsExtension** cmdlet gets the settings of the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="f5509-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5509-107">EXAMPLES</span></span>

### <span data-ttu-id="f5509-108">Exempel 1: få tillägget installerat på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="f5509-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVMDiagnosticsExtension -VM $VM
```

<span data-ttu-id="f5509-109">Det här kommandot får tillägget Använd för den angivna virtuella datorn enligt variabeln $VM.</span><span class="sxs-lookup"><span data-stu-id="f5509-109">This command gets the diagnostics extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="f5509-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5509-110">PARAMETERS</span></span>

### <span data-ttu-id="f5509-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f5509-111">-InformationAction</span></span>
<span data-ttu-id="f5509-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="f5509-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f5509-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f5509-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5509-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="f5509-114">Continue</span></span>
- <span data-ttu-id="f5509-115">Över</span><span class="sxs-lookup"><span data-stu-id="f5509-115">Ignore</span></span>
- <span data-ttu-id="f5509-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="f5509-116">Inquire</span></span>
- <span data-ttu-id="f5509-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f5509-117">SilentlyContinue</span></span>
- <span data-ttu-id="f5509-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="f5509-118">Stop</span></span>
- <span data-ttu-id="f5509-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="f5509-119">Suspend</span></span>

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

### <span data-ttu-id="f5509-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f5509-120">-InformationVariable</span></span>
<span data-ttu-id="f5509-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="f5509-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f5509-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="f5509-122">-Profile</span></span>
<span data-ttu-id="f5509-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f5509-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5509-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f5509-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5509-125">-VM</span><span class="sxs-lookup"><span data-stu-id="f5509-125">-VM</span></span>
<span data-ttu-id="f5509-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="f5509-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f5509-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5509-127">CommonParameters</span></span>
<span data-ttu-id="f5509-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5509-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5509-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5509-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5509-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5509-130">INPUTS</span></span>

## <span data-ttu-id="f5509-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5509-131">OUTPUTS</span></span>

## <span data-ttu-id="f5509-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5509-132">NOTES</span></span>

## <span data-ttu-id="f5509-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5509-133">RELATED LINKS</span></span>

[<span data-ttu-id="f5509-134">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f5509-134">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="f5509-135">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f5509-135">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)


