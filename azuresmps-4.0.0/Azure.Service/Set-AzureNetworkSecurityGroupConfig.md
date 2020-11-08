---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8E64309-7AF6-4439-841E-922B11C072AA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15dd195b86e70ad0a95484417d8cf87b0e544920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093482"
---
# <span data-ttu-id="ea7ba-101">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="ea7ba-101">Set-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="ea7ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea7ba-102">SYNOPSIS</span></span>

## <span data-ttu-id="ea7ba-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea7ba-103">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupConfig [-NetworkSecurityGroupName] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea7ba-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea7ba-104">DESCRIPTION</span></span>

## <span data-ttu-id="ea7ba-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea7ba-105">EXAMPLES</span></span>

### <span data-ttu-id="ea7ba-106">9.1</span><span class="sxs-lookup"><span data-stu-id="ea7ba-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ea7ba-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea7ba-107">PARAMETERS</span></span>

### <span data-ttu-id="ea7ba-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea7ba-108">-InformationAction</span></span>
<span data-ttu-id="ea7ba-109">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea7ba-110">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ea7ba-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea7ba-111">Vidare</span><span class="sxs-lookup"><span data-stu-id="ea7ba-111">Continue</span></span>
- <span data-ttu-id="ea7ba-112">Över</span><span class="sxs-lookup"><span data-stu-id="ea7ba-112">Ignore</span></span>
- <span data-ttu-id="ea7ba-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="ea7ba-113">Inquire</span></span>
- <span data-ttu-id="ea7ba-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea7ba-114">SilentlyContinue</span></span>
- <span data-ttu-id="ea7ba-115">Stanna</span><span class="sxs-lookup"><span data-stu-id="ea7ba-115">Stop</span></span>
- <span data-ttu-id="ea7ba-116">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ea7ba-116">Suspend</span></span>

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

### <span data-ttu-id="ea7ba-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea7ba-117">-InformationVariable</span></span>
<span data-ttu-id="ea7ba-118">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ea7ba-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7ba-119">-NetworkSecurityGroupName</span></span>
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

### <span data-ttu-id="ea7ba-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="ea7ba-120">-Profile</span></span>
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

### <span data-ttu-id="ea7ba-121">-VM</span><span class="sxs-lookup"><span data-stu-id="ea7ba-121">-VM</span></span>
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

### <span data-ttu-id="ea7ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7ba-122">CommonParameters</span></span>
<span data-ttu-id="ea7ba-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7ba-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7ba-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7ba-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea7ba-125">INPUTS</span></span>

## <span data-ttu-id="ea7ba-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea7ba-126">OUTPUTS</span></span>

## <span data-ttu-id="ea7ba-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea7ba-127">NOTES</span></span>

## <span data-ttu-id="ea7ba-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea7ba-128">RELATED LINKS</span></span>

[<span data-ttu-id="ea7ba-129">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="ea7ba-129">Remove-AzureNetworkSecurityGroupConfig</span></span>](./Remove-AzureNetworkSecurityGroupConfig.md)


