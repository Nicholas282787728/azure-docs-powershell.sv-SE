---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099601"
---
# <span data-ttu-id="50d70-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="50d70-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="50d70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50d70-102">SYNOPSIS</span></span>

<span data-ttu-id="50d70-103">Får Azure Automation-konton.</span><span class="sxs-lookup"><span data-stu-id="50d70-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="50d70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50d70-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="50d70-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50d70-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="50d70-106">Cmdleten **Get-AzureAutomationAccount** hämtar Microsoft Azure Automation-kontona för din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="50d70-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="50d70-107">Ett Automation-konto är en behållare för Automation-resurser som är isolerade från andra Automation-konton.</span><span class="sxs-lookup"><span data-stu-id="50d70-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="50d70-108">Automatiserings resurser inkluderar Runbooks, jobb och till gångar.</span><span class="sxs-lookup"><span data-stu-id="50d70-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="50d70-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50d70-109">EXAMPLES</span></span>

### <span data-ttu-id="50d70-110">Exempel 1: skaffa ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="50d70-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="50d70-111">Det här kommandot får Automation-kontot Contoso17.</span><span class="sxs-lookup"><span data-stu-id="50d70-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="50d70-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50d70-112">PARAMETERS</span></span>

### <span data-ttu-id="50d70-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="50d70-113">-Location</span></span>
<span data-ttu-id="50d70-114">Anger en Azure-plats som är kopplad till automatiserings konton.</span><span class="sxs-lookup"><span data-stu-id="50d70-114">Specifies an Azure location associated with Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d70-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="50d70-115">-Name</span></span>
<span data-ttu-id="50d70-116">Anger namnet på ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="50d70-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d70-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="50d70-117">-Profile</span></span>
<span data-ttu-id="50d70-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="50d70-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50d70-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="50d70-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50d70-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d70-120">CommonParameters</span></span>
<span data-ttu-id="50d70-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d70-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d70-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d70-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d70-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50d70-123">INPUTS</span></span>

## <span data-ttu-id="50d70-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50d70-124">OUTPUTS</span></span>

### <span data-ttu-id="50d70-125">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="50d70-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="50d70-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50d70-126">NOTES</span></span>

## <span data-ttu-id="50d70-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50d70-127">RELATED LINKS</span></span>

[<span data-ttu-id="50d70-128">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="50d70-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="50d70-129">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="50d70-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


