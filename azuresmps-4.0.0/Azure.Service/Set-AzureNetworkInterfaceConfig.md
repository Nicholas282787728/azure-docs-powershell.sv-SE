---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A4E88106-1B47-4ACD-8F35-027D16EA7791
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b3422581fa884245807f258adcc31d52404c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099035"
---
# <span data-ttu-id="77955-101">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="77955-101">Set-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="77955-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77955-102">SYNOPSIS</span></span>

## <span data-ttu-id="77955-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77955-103">SYNTAX</span></span>

```
Set-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="77955-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77955-104">DESCRIPTION</span></span>

## <span data-ttu-id="77955-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77955-105">EXAMPLES</span></span>

### <span data-ttu-id="77955-106">9.1</span><span class="sxs-lookup"><span data-stu-id="77955-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="77955-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77955-107">PARAMETERS</span></span>

### <span data-ttu-id="77955-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="77955-108">-InformationAction</span></span>
<span data-ttu-id="77955-109">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="77955-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="77955-110">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="77955-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77955-111">Vidare</span><span class="sxs-lookup"><span data-stu-id="77955-111">Continue</span></span>
- <span data-ttu-id="77955-112">Över</span><span class="sxs-lookup"><span data-stu-id="77955-112">Ignore</span></span>
- <span data-ttu-id="77955-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="77955-113">Inquire</span></span>
- <span data-ttu-id="77955-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="77955-114">SilentlyContinue</span></span>
- <span data-ttu-id="77955-115">Stanna</span><span class="sxs-lookup"><span data-stu-id="77955-115">Stop</span></span>
- <span data-ttu-id="77955-116">Avbryt</span><span class="sxs-lookup"><span data-stu-id="77955-116">Suspend</span></span>

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

### <span data-ttu-id="77955-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="77955-117">-InformationVariable</span></span>
<span data-ttu-id="77955-118">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="77955-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="77955-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="77955-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77955-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="77955-120">-Name</span></span>
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

### <span data-ttu-id="77955-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77955-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77955-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="77955-122">-Profile</span></span>
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

### <span data-ttu-id="77955-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="77955-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77955-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="77955-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77955-125">-VM</span><span class="sxs-lookup"><span data-stu-id="77955-125">-VM</span></span>
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

### <span data-ttu-id="77955-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77955-126">CommonParameters</span></span>
<span data-ttu-id="77955-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77955-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77955-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77955-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77955-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77955-129">INPUTS</span></span>

## <span data-ttu-id="77955-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77955-130">OUTPUTS</span></span>

## <span data-ttu-id="77955-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77955-131">NOTES</span></span>

## <span data-ttu-id="77955-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77955-132">RELATED LINKS</span></span>

[<span data-ttu-id="77955-133">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="77955-133">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="77955-134">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="77955-134">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="77955-135">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="77955-135">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)


