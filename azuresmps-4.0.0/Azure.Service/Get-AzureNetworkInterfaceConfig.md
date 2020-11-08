---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099814"
---
# <span data-ttu-id="b898a-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="b898a-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="b898a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b898a-102">SYNOPSIS</span></span>

## <span data-ttu-id="b898a-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b898a-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b898a-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b898a-104">DESCRIPTION</span></span>

## <span data-ttu-id="b898a-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b898a-105">EXAMPLES</span></span>

### <span data-ttu-id="b898a-106">9.1</span><span class="sxs-lookup"><span data-stu-id="b898a-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b898a-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b898a-107">PARAMETERS</span></span>

### <span data-ttu-id="b898a-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b898a-108">-InformationAction</span></span>
<span data-ttu-id="b898a-109">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="b898a-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b898a-110">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b898a-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b898a-111">Vidare</span><span class="sxs-lookup"><span data-stu-id="b898a-111">Continue</span></span>
- <span data-ttu-id="b898a-112">Över</span><span class="sxs-lookup"><span data-stu-id="b898a-112">Ignore</span></span>
- <span data-ttu-id="b898a-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="b898a-113">Inquire</span></span>
- <span data-ttu-id="b898a-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b898a-114">SilentlyContinue</span></span>
- <span data-ttu-id="b898a-115">Stanna</span><span class="sxs-lookup"><span data-stu-id="b898a-115">Stop</span></span>
- <span data-ttu-id="b898a-116">Avbryt</span><span class="sxs-lookup"><span data-stu-id="b898a-116">Suspend</span></span>

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

### <span data-ttu-id="b898a-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b898a-117">-InformationVariable</span></span>
<span data-ttu-id="b898a-118">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="b898a-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b898a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b898a-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b898a-120">-VM</span><span class="sxs-lookup"><span data-stu-id="b898a-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b898a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b898a-121">CommonParameters</span></span>
<span data-ttu-id="b898a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b898a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b898a-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b898a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b898a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b898a-124">INPUTS</span></span>

## <span data-ttu-id="b898a-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b898a-125">OUTPUTS</span></span>

## <span data-ttu-id="b898a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b898a-126">NOTES</span></span>

## <span data-ttu-id="b898a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b898a-127">RELATED LINKS</span></span>

[<span data-ttu-id="b898a-128">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="b898a-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="b898a-129">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="b898a-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="b898a-130">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="b898a-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


