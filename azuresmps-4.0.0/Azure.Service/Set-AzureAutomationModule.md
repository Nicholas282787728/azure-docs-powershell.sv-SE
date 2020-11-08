---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099060"
---
# <span data-ttu-id="f1420-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f1420-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="f1420-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1420-102">SYNOPSIS</span></span>

<span data-ttu-id="f1420-103">Uppdaterar en modul i Automation.</span><span class="sxs-lookup"><span data-stu-id="f1420-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="f1420-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1420-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1420-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1420-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f1420-106">Cmdleten **set-AzureAutomationModule** importerar en ny version av en modul eller ändrar konfigurationen för modulen i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f1420-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="f1420-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1420-107">EXAMPLES</span></span>

### <span data-ttu-id="f1420-108">Exempel 1: uppdatera en modul</span><span class="sxs-lookup"><span data-stu-id="f1420-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="f1420-109">Det här kommandot importerar en uppdaterad version av en befintlig modul som heter ContosoModule till det Azure Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f1420-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f1420-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1420-110">PARAMETERS</span></span>

### <span data-ttu-id="f1420-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f1420-111">-AutomationAccountName</span></span>
<span data-ttu-id="f1420-112">Anger namnet på Automation-kontot med modulen.</span><span class="sxs-lookup"><span data-stu-id="f1420-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="f1420-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="f1420-113">-ContentLinkUri</span></span>
<span data-ttu-id="f1420-114">Anger sökvägen till modul filen.</span><span class="sxs-lookup"><span data-stu-id="f1420-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1420-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="f1420-115">-ContentLinkVersion</span></span>
<span data-ttu-id="f1420-116">Anger vilken version av modulen det är.</span><span class="sxs-lookup"><span data-stu-id="f1420-116">Specifies the version of the module.</span></span>

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

### <span data-ttu-id="f1420-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1420-117">-Name</span></span>
<span data-ttu-id="f1420-118">Anger namnet på modulen.</span><span class="sxs-lookup"><span data-stu-id="f1420-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="f1420-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="f1420-119">-Profile</span></span>
<span data-ttu-id="f1420-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f1420-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f1420-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f1420-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1420-122">-Taggar</span><span class="sxs-lookup"><span data-stu-id="f1420-122">-Tags</span></span>
<span data-ttu-id="f1420-123">Anger taggar för modulen.</span><span class="sxs-lookup"><span data-stu-id="f1420-123">Specifies tags for the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1420-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1420-124">CommonParameters</span></span>
<span data-ttu-id="f1420-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1420-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1420-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1420-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1420-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1420-127">INPUTS</span></span>

### <span data-ttu-id="f1420-128">Microsoft. Azure. commands. Automation. Model. modul</span><span class="sxs-lookup"><span data-stu-id="f1420-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="f1420-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1420-129">OUTPUTS</span></span>

## <span data-ttu-id="f1420-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1420-130">NOTES</span></span>

## <span data-ttu-id="f1420-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1420-131">RELATED LINKS</span></span>

[<span data-ttu-id="f1420-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f1420-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="f1420-133">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f1420-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="f1420-134">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f1420-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


