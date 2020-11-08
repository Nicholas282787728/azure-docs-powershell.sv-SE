---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099657"
---
# <span data-ttu-id="60abf-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="60abf-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="60abf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60abf-102">SYNOPSIS</span></span>

<span data-ttu-id="60abf-103">Ändrar värdet för ett fält för en anslutning.</span><span class="sxs-lookup"><span data-stu-id="60abf-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="60abf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60abf-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="60abf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60abf-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="60abf-106">Cmdleten **set-AzureAutomationConnectionFieldValue** ändrar värdet för ett fält för en anslutning i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="60abf-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="60abf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60abf-107">EXAMPLES</span></span>

## <span data-ttu-id="60abf-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60abf-108">PARAMETERS</span></span>

### <span data-ttu-id="60abf-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60abf-109">-AutomationAccountName</span></span>
<span data-ttu-id="60abf-110">Anger namnet på Automation-kontot med anslutningen.</span><span class="sxs-lookup"><span data-stu-id="60abf-110">Specifies the name of the Automation account with the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60abf-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="60abf-111">-ConnectionFieldName</span></span>
<span data-ttu-id="60abf-112">Anger ett namn för fältet.</span><span class="sxs-lookup"><span data-stu-id="60abf-112">Specifies a name for the field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60abf-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="60abf-113">-Name</span></span>
<span data-ttu-id="60abf-114">Anger ett namn för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="60abf-114">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60abf-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="60abf-115">-Profile</span></span>
<span data-ttu-id="60abf-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="60abf-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="60abf-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="60abf-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="60abf-118">-Värde</span><span class="sxs-lookup"><span data-stu-id="60abf-118">-Value</span></span>
<span data-ttu-id="60abf-119">Anger ett värde för att lagra i fältet Connection.</span><span class="sxs-lookup"><span data-stu-id="60abf-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60abf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60abf-120">CommonParameters</span></span>
<span data-ttu-id="60abf-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60abf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60abf-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60abf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60abf-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60abf-123">INPUTS</span></span>

## <span data-ttu-id="60abf-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60abf-124">OUTPUTS</span></span>

## <span data-ttu-id="60abf-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60abf-125">NOTES</span></span>

## <span data-ttu-id="60abf-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60abf-126">RELATED LINKS</span></span>

[<span data-ttu-id="60abf-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="60abf-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="60abf-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="60abf-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="60abf-129">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="60abf-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


