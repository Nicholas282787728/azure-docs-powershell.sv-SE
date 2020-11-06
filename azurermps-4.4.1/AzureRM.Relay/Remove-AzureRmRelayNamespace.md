---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: d0ac732a0feaffa187ec33d60f9587a7a6a1cff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583799"
---
# <span data-ttu-id="dc043-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="dc043-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="dc043-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc043-102">SYNOPSIS</span></span>
<span data-ttu-id="dc043-103">Tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dc043-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc043-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc043-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc043-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc043-105">DESCRIPTION</span></span>
<span data-ttu-id="dc043-106">Cmdleten **Remove-AzureRmRelayNamespace** tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dc043-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="dc043-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc043-107">EXAMPLES</span></span>

### <span data-ttu-id="dc043-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc043-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="dc043-109">Tar bort relä namnområdet `TestNameSpace-Relay1` från den angivna resurs gruppen `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="dc043-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="dc043-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc043-110">PARAMETERS</span></span>

### <span data-ttu-id="dc043-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc043-111">-Name</span></span>
<span data-ttu-id="dc043-112">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="dc043-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="dc043-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc043-113">-ResourceGroupName</span></span>
<span data-ttu-id="dc043-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="dc043-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc043-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc043-115">-Confirm</span></span>
<span data-ttu-id="dc043-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc043-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc043-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc043-117">-WhatIf</span></span>
<span data-ttu-id="dc043-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc043-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc043-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc043-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc043-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc043-120">-DefaultProfile</span></span>
<span data-ttu-id="dc043-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc043-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc043-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc043-122">CommonParameters</span></span>
<span data-ttu-id="dc043-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc043-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc043-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc043-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc043-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc043-125">INPUTS</span></span>

### <span data-ttu-id="dc043-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc043-126">-ResourceGroupName</span></span>
 <span data-ttu-id="dc043-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dc043-127">System.String</span></span>

### <span data-ttu-id="dc043-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc043-128">-Name</span></span>
 <span data-ttu-id="dc043-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dc043-129">System.String</span></span>

## <span data-ttu-id="dc043-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc043-130">OUTPUTS</span></span>

### <span data-ttu-id="dc043-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="dc043-131">System.Object</span></span>

## <span data-ttu-id="dc043-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc043-132">NOTES</span></span>

## <span data-ttu-id="dc043-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc043-133">RELATED LINKS</span></span>

