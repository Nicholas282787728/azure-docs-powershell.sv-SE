---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099696"
---
# <span data-ttu-id="187fe-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="187fe-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="187fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="187fe-102">SYNOPSIS</span></span>

## <span data-ttu-id="187fe-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="187fe-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="187fe-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="187fe-104">DESCRIPTION</span></span>

## <span data-ttu-id="187fe-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="187fe-105">EXAMPLES</span></span>

### <span data-ttu-id="187fe-106">9.1</span><span class="sxs-lookup"><span data-stu-id="187fe-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="187fe-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="187fe-107">PARAMETERS</span></span>

### <span data-ttu-id="187fe-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="187fe-108">-InformationAction</span></span>
<span data-ttu-id="187fe-109">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="187fe-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="187fe-110">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="187fe-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="187fe-111">Vidare</span><span class="sxs-lookup"><span data-stu-id="187fe-111">Continue</span></span>
- <span data-ttu-id="187fe-112">Över</span><span class="sxs-lookup"><span data-stu-id="187fe-112">Ignore</span></span>
- <span data-ttu-id="187fe-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="187fe-113">Inquire</span></span>
- <span data-ttu-id="187fe-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="187fe-114">SilentlyContinue</span></span>
- <span data-ttu-id="187fe-115">Stanna</span><span class="sxs-lookup"><span data-stu-id="187fe-115">Stop</span></span>
- <span data-ttu-id="187fe-116">Avbryt</span><span class="sxs-lookup"><span data-stu-id="187fe-116">Suspend</span></span>

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

### <span data-ttu-id="187fe-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="187fe-117">-InformationVariable</span></span>
<span data-ttu-id="187fe-118">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="187fe-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="187fe-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="187fe-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187fe-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="187fe-120">-Profile</span></span>
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

### <span data-ttu-id="187fe-121">-VM</span><span class="sxs-lookup"><span data-stu-id="187fe-121">-VM</span></span>
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

### <span data-ttu-id="187fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187fe-122">CommonParameters</span></span>
<span data-ttu-id="187fe-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="187fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187fe-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187fe-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="187fe-125">INPUTS</span></span>

## <span data-ttu-id="187fe-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="187fe-126">OUTPUTS</span></span>

## <span data-ttu-id="187fe-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="187fe-127">NOTES</span></span>

## <span data-ttu-id="187fe-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="187fe-128">RELATED LINKS</span></span>

[<span data-ttu-id="187fe-129">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="187fe-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="187fe-130">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="187fe-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="187fe-131">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="187fe-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


