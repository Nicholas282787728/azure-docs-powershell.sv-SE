---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: a774f388690ab2ee0528e94a2a96addecf1687fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585351"
---
# <span data-ttu-id="f7d22-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="f7d22-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="f7d22-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7d22-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d22-103">Tar bort WcfRelay från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="f7d22-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7d22-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7d22-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d22-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7d22-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d22-106">Cmdleten **Remove-AzureRmWcfRelay** tar bort WcfRelay från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="f7d22-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="f7d22-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7d22-107">EXAMPLES</span></span>

### <span data-ttu-id="f7d22-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f7d22-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="f7d22-109">Tar bort WcfRelay `TestWCFRelay1` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="f7d22-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="f7d22-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7d22-110">PARAMETERS</span></span>

### <span data-ttu-id="f7d22-111">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f7d22-111">-Namespace</span></span>
<span data-ttu-id="f7d22-112">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="f7d22-112">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d22-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d22-113">-ResourceGroupName</span></span>
<span data-ttu-id="f7d22-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f7d22-114">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d22-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7d22-115">-Name</span></span>
<span data-ttu-id="f7d22-116">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="f7d22-116">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d22-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7d22-117">-Confirm</span></span>
<span data-ttu-id="f7d22-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7d22-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d22-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d22-119">-WhatIf</span></span>
<span data-ttu-id="f7d22-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7d22-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d22-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7d22-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d22-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d22-122">-DefaultProfile</span></span>
<span data-ttu-id="f7d22-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d22-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d22-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d22-124">CommonParameters</span></span>
<span data-ttu-id="f7d22-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d22-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d22-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7d22-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d22-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7d22-127">INPUTS</span></span>

### <span data-ttu-id="f7d22-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d22-128">-ResourceGroupName</span></span>
 <span data-ttu-id="f7d22-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f7d22-129">System.String</span></span>
 

### <span data-ttu-id="f7d22-130">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f7d22-130">-Namespace</span></span>
 <span data-ttu-id="f7d22-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f7d22-131">System.String</span></span>
 

### <span data-ttu-id="f7d22-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7d22-132">-Name</span></span>
 <span data-ttu-id="f7d22-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f7d22-133">System.String</span></span>

## <span data-ttu-id="f7d22-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7d22-134">OUTPUTS</span></span>

### <span data-ttu-id="f7d22-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7d22-135">System.Object</span></span>

## <span data-ttu-id="f7d22-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7d22-136">NOTES</span></span>

## <span data-ttu-id="f7d22-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7d22-137">RELATED LINKS</span></span>

