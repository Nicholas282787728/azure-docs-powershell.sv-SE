---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 5e49497f8784e9686c84cb75dde4b8fd4297578d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576123"
---
# <span data-ttu-id="f4a4c-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="f4a4c-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="f4a4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a4c-103">Tar bort WcfRelay från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4a4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4a4c-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4a4c-105">DESCRIPTION</span></span>
<span data-ttu-id="f4a4c-106">Cmdleten **Remove-AzureRmWcfRelay** tar bort WcfRelay från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="f4a4c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4a4c-107">EXAMPLES</span></span>

### <span data-ttu-id="f4a4c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4a4c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="f4a4c-109">Tar bort WcfRelay `TestWCFRelay1` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="f4a4c-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="f4a4c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4a4c-110">PARAMETERS</span></span>

### <span data-ttu-id="f4a4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a4c-111">-DefaultProfile</span></span>
<span data-ttu-id="f4a4c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4a4c-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4a4c-113">-Name</span></span>
<span data-ttu-id="f4a4c-114">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f4a4c-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f4a4c-115">-Namespace</span></span>
<span data-ttu-id="f4a4c-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-116">Namespace Name.</span></span>

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

### <span data-ttu-id="f4a4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4a4c-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="f4a4c-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4a4c-119">-Confirm</span></span>
<span data-ttu-id="f4a4c-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a4c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a4c-121">-WhatIf</span></span>
<span data-ttu-id="f4a4c-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a4c-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a4c-124">CommonParameters</span></span>
<span data-ttu-id="f4a4c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f4a4c-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a4c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a4c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4a4c-127">INPUTS</span></span>

### <span data-ttu-id="f4a4c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f4a4c-128">System.String</span></span>


## <span data-ttu-id="f4a4c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4a4c-129">OUTPUTS</span></span>

### <span data-ttu-id="f4a4c-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="f4a4c-130">System.Void</span></span>


## <span data-ttu-id="f4a4c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4a4c-131">NOTES</span></span>

## <span data-ttu-id="f4a4c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4a4c-132">RELATED LINKS</span></span>
