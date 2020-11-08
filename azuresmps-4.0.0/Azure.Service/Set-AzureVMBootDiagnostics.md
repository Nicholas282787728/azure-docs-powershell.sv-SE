---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099023"
---
# <span data-ttu-id="4f79c-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4f79c-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="4f79c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f79c-102">SYNOPSIS</span></span>

## <span data-ttu-id="4f79c-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f79c-103">SYNTAX</span></span>

### <span data-ttu-id="4f79c-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4f79c-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4f79c-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4f79c-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f79c-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f79c-106">DESCRIPTION</span></span>

## <span data-ttu-id="4f79c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f79c-107">EXAMPLES</span></span>

### <span data-ttu-id="4f79c-108">9.1</span><span class="sxs-lookup"><span data-stu-id="4f79c-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="4f79c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f79c-109">PARAMETERS</span></span>

### <span data-ttu-id="4f79c-110">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="4f79c-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f79c-111">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="4f79c-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f79c-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4f79c-112">-InformationAction</span></span>
<span data-ttu-id="4f79c-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4f79c-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f79c-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4f79c-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f79c-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="4f79c-115">Continue</span></span>
- <span data-ttu-id="4f79c-116">Över</span><span class="sxs-lookup"><span data-stu-id="4f79c-116">Ignore</span></span>
- <span data-ttu-id="4f79c-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="4f79c-117">Inquire</span></span>
- <span data-ttu-id="4f79c-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f79c-118">SilentlyContinue</span></span>
- <span data-ttu-id="4f79c-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="4f79c-119">Stop</span></span>
- <span data-ttu-id="4f79c-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4f79c-120">Suspend</span></span>

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

### <span data-ttu-id="4f79c-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f79c-121">-InformationVariable</span></span>
<span data-ttu-id="4f79c-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4f79c-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f79c-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f79c-123">-Profile</span></span>
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

### <span data-ttu-id="4f79c-124">-VM</span><span class="sxs-lookup"><span data-stu-id="4f79c-124">-VM</span></span>
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

### <span data-ttu-id="4f79c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f79c-125">CommonParameters</span></span>
<span data-ttu-id="4f79c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f79c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f79c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f79c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f79c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f79c-128">INPUTS</span></span>

## <span data-ttu-id="4f79c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f79c-129">OUTPUTS</span></span>

## <span data-ttu-id="4f79c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f79c-130">NOTES</span></span>

## <span data-ttu-id="4f79c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f79c-131">RELATED LINKS</span></span>

