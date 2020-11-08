---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099725"
---
# <span data-ttu-id="11489-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="11489-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="11489-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11489-102">SYNOPSIS</span></span>

<span data-ttu-id="11489-103">Tar bort ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="11489-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="11489-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11489-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11489-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11489-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="11489-106">Cmdleten **Remove-AzureAutomationAccount** tar bort ett konto från Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="11489-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="11489-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11489-107">EXAMPLES</span></span>

### <span data-ttu-id="11489-108">Exempel 1: ta bort ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="11489-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="11489-109">Det här kommandot tar bort ett Automation-konto med namnet MyAutomationAccount utan att fråga efter användar verifiering.</span><span class="sxs-lookup"><span data-stu-id="11489-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="11489-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11489-110">PARAMETERS</span></span>

### <span data-ttu-id="11489-111">-Force</span><span class="sxs-lookup"><span data-stu-id="11489-111">-Force</span></span>
<span data-ttu-id="11489-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="11489-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11489-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="11489-113">-Name</span></span>
<span data-ttu-id="11489-114">Anger namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="11489-114">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11489-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="11489-115">-Profile</span></span>
<span data-ttu-id="11489-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="11489-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11489-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="11489-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11489-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11489-118">CommonParameters</span></span>
<span data-ttu-id="11489-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11489-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11489-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11489-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11489-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11489-121">INPUTS</span></span>

## <span data-ttu-id="11489-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11489-122">OUTPUTS</span></span>

## <span data-ttu-id="11489-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11489-123">NOTES</span></span>

## <span data-ttu-id="11489-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11489-124">RELATED LINKS</span></span>

[<span data-ttu-id="11489-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="11489-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="11489-126">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="11489-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


