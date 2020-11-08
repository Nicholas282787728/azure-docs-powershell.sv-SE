---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093220"
---
# <span data-ttu-id="fcf94-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fcf94-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="fcf94-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcf94-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf94-103">Tar bort en Azure Virtual Machine SQL Server-tillägg från ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="fcf94-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="fcf94-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcf94-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fcf94-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcf94-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf94-106">Cmdleten **Remove-AzureVMSqlServerExtension** tar bort ett SQL Server-tillägg för Azure Virtual Machine från ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="fcf94-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="fcf94-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcf94-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf94-108">9.1</span><span class="sxs-lookup"><span data-stu-id="fcf94-108">1:</span></span>
```

```

## <span data-ttu-id="fcf94-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcf94-109">PARAMETERS</span></span>

### <span data-ttu-id="fcf94-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fcf94-110">-InformationAction</span></span>
<span data-ttu-id="fcf94-111">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="fcf94-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fcf94-112">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fcf94-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fcf94-113">Vidare</span><span class="sxs-lookup"><span data-stu-id="fcf94-113">Continue</span></span>
- <span data-ttu-id="fcf94-114">Över</span><span class="sxs-lookup"><span data-stu-id="fcf94-114">Ignore</span></span>
- <span data-ttu-id="fcf94-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="fcf94-115">Inquire</span></span>
- <span data-ttu-id="fcf94-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fcf94-116">SilentlyContinue</span></span>
- <span data-ttu-id="fcf94-117">Stanna</span><span class="sxs-lookup"><span data-stu-id="fcf94-117">Stop</span></span>
- <span data-ttu-id="fcf94-118">Avbryt</span><span class="sxs-lookup"><span data-stu-id="fcf94-118">Suspend</span></span>

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

### <span data-ttu-id="fcf94-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fcf94-119">-InformationVariable</span></span>
<span data-ttu-id="fcf94-120">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="fcf94-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fcf94-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="fcf94-121">-Profile</span></span>
<span data-ttu-id="fcf94-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fcf94-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fcf94-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fcf94-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fcf94-124">-VM</span><span class="sxs-lookup"><span data-stu-id="fcf94-124">-VM</span></span>
<span data-ttu-id="fcf94-125">Anger det beständiga virtuella dator objekt som denna cmdlet tar bort tillägget från.</span><span class="sxs-lookup"><span data-stu-id="fcf94-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="fcf94-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf94-126">CommonParameters</span></span>
<span data-ttu-id="fcf94-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf94-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf94-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf94-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf94-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcf94-129">INPUTS</span></span>

## <span data-ttu-id="fcf94-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcf94-130">OUTPUTS</span></span>

## <span data-ttu-id="fcf94-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcf94-131">NOTES</span></span>

## <span data-ttu-id="fcf94-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcf94-132">RELATED LINKS</span></span>

[<span data-ttu-id="fcf94-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fcf94-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="fcf94-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fcf94-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


