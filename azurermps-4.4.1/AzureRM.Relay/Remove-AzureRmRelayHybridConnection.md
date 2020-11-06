---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7f65f77d9d1f525dd8850c6934263b608d241751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582223"
---
# <span data-ttu-id="5c47d-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="5c47d-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="5c47d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c47d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c47d-103">Tar bort HybridConnection från det angivna HybridConnection-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="5c47d-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c47d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c47d-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c47d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c47d-105">DESCRIPTION</span></span>
<span data-ttu-id="5c47d-106">Cmdleten **Remove-AzureRmRelayHybridConnection** tar bort HybridConnection från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="5c47d-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="5c47d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c47d-107">EXAMPLES</span></span>

### <span data-ttu-id="5c47d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c47d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="5c47d-109">Tar bort HybridConnection `TestHybridConnection` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="5c47d-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="5c47d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c47d-110">PARAMETERS</span></span>

### <span data-ttu-id="5c47d-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c47d-111">-Name</span></span>
<span data-ttu-id="5c47d-112">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="5c47d-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="5c47d-113">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5c47d-113">-Namespace</span></span>
<span data-ttu-id="5c47d-114">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="5c47d-114">Namespace Name.</span></span>

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

### <span data-ttu-id="5c47d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c47d-115">-ResourceGroupName</span></span>
<span data-ttu-id="5c47d-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5c47d-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c47d-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c47d-117">-Confirm</span></span>
<span data-ttu-id="5c47d-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c47d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c47d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c47d-119">-WhatIf</span></span>
<span data-ttu-id="5c47d-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c47d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c47d-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c47d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c47d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c47d-122">-DefaultProfile</span></span>
<span data-ttu-id="5c47d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c47d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c47d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c47d-124">CommonParameters</span></span>
<span data-ttu-id="5c47d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c47d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c47d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c47d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c47d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c47d-127">INPUTS</span></span>

### <span data-ttu-id="5c47d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c47d-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="5c47d-129">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5c47d-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="5c47d-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c47d-130">-Name</span></span>
    System.String

## <span data-ttu-id="5c47d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c47d-131">OUTPUTS</span></span>

### <span data-ttu-id="5c47d-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="5c47d-132">System.Object</span></span>

## <span data-ttu-id="5c47d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c47d-133">NOTES</span></span>

## <span data-ttu-id="5c47d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c47d-134">RELATED LINKS</span></span>

