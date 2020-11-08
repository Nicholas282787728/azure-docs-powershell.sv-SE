---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4370FF88-E34F-499D-AF57-53C15B4EB6E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: e55d9e54dcaa0f547d64ec58b2772a581a8ec30a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099714"
---
# <span data-ttu-id="4107d-101">Remove-AzureAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="4107d-101">Remove-AzureAutomationConnectionType</span></span>

## <span data-ttu-id="4107d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4107d-102">SYNOPSIS</span></span>

<span data-ttu-id="4107d-103">Tar bort en Anslutnings typ.</span><span class="sxs-lookup"><span data-stu-id="4107d-103">Removes a connection type.</span></span>

## <span data-ttu-id="4107d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4107d-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnectionType -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4107d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4107d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4107d-106">Cmdleten **Remove-AzureAutomationConnectionType** tar bort en Anslutnings typ för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4107d-106">The **Remove-AzureAutomationConnectionType** cmdlet removes an Azure Automation connection type.</span></span>

## <span data-ttu-id="4107d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4107d-107">EXAMPLES</span></span>

## <span data-ttu-id="4107d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4107d-108">PARAMETERS</span></span>

### <span data-ttu-id="4107d-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4107d-109">-AutomationAccountName</span></span>
<span data-ttu-id="4107d-110">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="4107d-110">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4107d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4107d-111">-Force</span></span>
<span data-ttu-id="4107d-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4107d-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4107d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4107d-113">-Name</span></span>
<span data-ttu-id="4107d-114">Anger namnet på den typ av anslutning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4107d-114">Specifies the name of the connection type to remove.</span></span>

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

### <span data-ttu-id="4107d-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="4107d-115">-Profile</span></span>
<span data-ttu-id="4107d-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4107d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4107d-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4107d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4107d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4107d-118">CommonParameters</span></span>
<span data-ttu-id="4107d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4107d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4107d-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4107d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4107d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4107d-121">INPUTS</span></span>

## <span data-ttu-id="4107d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4107d-122">OUTPUTS</span></span>

## <span data-ttu-id="4107d-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4107d-123">NOTES</span></span>

## <span data-ttu-id="4107d-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4107d-124">RELATED LINKS</span></span>

