---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099723"
---
# <span data-ttu-id="ce5de-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5de-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="ce5de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce5de-102">SYNOPSIS</span></span>

<span data-ttu-id="ce5de-103">Tar bort ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="ce5de-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="ce5de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce5de-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce5de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce5de-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ce5de-106">Cmdleten **Remove-AzureAutomationAccount** tar bort ett certifikat från Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ce5de-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="ce5de-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce5de-107">EXAMPLES</span></span>

### <span data-ttu-id="ce5de-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="ce5de-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="ce5de-109">Det här kommandot tar bort ett certifikat som heter Cert01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ce5de-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ce5de-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce5de-110">PARAMETERS</span></span>

### <span data-ttu-id="ce5de-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce5de-111">-AutomationAccountName</span></span>
<span data-ttu-id="ce5de-112">Anger namnet på Automation-kontot med certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ce5de-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="ce5de-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ce5de-113">-Force</span></span>
<span data-ttu-id="ce5de-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ce5de-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce5de-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce5de-115">-Name</span></span>
<span data-ttu-id="ce5de-116">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ce5de-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="ce5de-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="ce5de-117">-Profile</span></span>
<span data-ttu-id="ce5de-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ce5de-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce5de-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ce5de-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce5de-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce5de-120">CommonParameters</span></span>
<span data-ttu-id="ce5de-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce5de-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce5de-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce5de-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce5de-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce5de-123">INPUTS</span></span>

## <span data-ttu-id="ce5de-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce5de-124">OUTPUTS</span></span>

## <span data-ttu-id="ce5de-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce5de-125">NOTES</span></span>

## <span data-ttu-id="ce5de-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce5de-126">RELATED LINKS</span></span>

[<span data-ttu-id="ce5de-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5de-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="ce5de-128">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5de-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="ce5de-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5de-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


