---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099454"
---
# <span data-ttu-id="36d40-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36d40-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="36d40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36d40-102">SYNOPSIS</span></span>

<span data-ttu-id="36d40-103">Skapar ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="36d40-103">Creates an Automation account.</span></span>

## <span data-ttu-id="36d40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36d40-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="36d40-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36d40-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="36d40-106">Cmdleten **New-AzureAutomationAccount** skapar ett nytt konto i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="36d40-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="36d40-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36d40-107">EXAMPLES</span></span>

### <span data-ttu-id="36d40-108">Exempel 1: skapa ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="36d40-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="36d40-109">Det här kommandot skapar ett Automation-konto med namnet MyAutomationAccount i USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="36d40-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="36d40-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36d40-110">PARAMETERS</span></span>

### <span data-ttu-id="36d40-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="36d40-111">-Location</span></span>
<span data-ttu-id="36d40-112">Anger platsen för kontot.</span><span class="sxs-lookup"><span data-stu-id="36d40-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="36d40-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="36d40-113">-Name</span></span>
<span data-ttu-id="36d40-114">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="36d40-114">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="36d40-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="36d40-115">-Profile</span></span>
<span data-ttu-id="36d40-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="36d40-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="36d40-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="36d40-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36d40-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d40-118">CommonParameters</span></span>
<span data-ttu-id="36d40-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d40-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d40-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d40-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d40-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36d40-121">INPUTS</span></span>

## <span data-ttu-id="36d40-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36d40-122">OUTPUTS</span></span>

### <span data-ttu-id="36d40-123">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36d40-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="36d40-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36d40-124">NOTES</span></span>

## <span data-ttu-id="36d40-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36d40-125">RELATED LINKS</span></span>

[<span data-ttu-id="36d40-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36d40-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="36d40-127">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36d40-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


