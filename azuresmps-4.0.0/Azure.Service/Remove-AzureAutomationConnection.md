---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099722"
---
# <span data-ttu-id="6f421-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6f421-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="6f421-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f421-102">SYNOPSIS</span></span>

<span data-ttu-id="6f421-103">Tar bort en anslutning från Automation.</span><span class="sxs-lookup"><span data-stu-id="6f421-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="6f421-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f421-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6f421-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f421-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6f421-106">Cmdleten **Remove-AzureAutomationConnection** tar bort en anslutning från Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6f421-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6f421-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f421-107">EXAMPLES</span></span>

### <span data-ttu-id="6f421-108">Exempel 1: ta bort en anslutning</span><span class="sxs-lookup"><span data-stu-id="6f421-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="6f421-109">Det här kommandot tar bort ett certifikat som heter min anslutning i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6f421-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6f421-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f421-110">PARAMETERS</span></span>

### <span data-ttu-id="6f421-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f421-111">-AutomationAccountName</span></span>
<span data-ttu-id="6f421-112">Anger namnet på Automation-kontot med autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="6f421-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="6f421-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6f421-113">-Force</span></span>
<span data-ttu-id="6f421-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6f421-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f421-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f421-115">-Name</span></span>
<span data-ttu-id="6f421-116">Anger namnet på anslutningen.</span><span class="sxs-lookup"><span data-stu-id="6f421-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="6f421-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="6f421-117">-Profile</span></span>
<span data-ttu-id="6f421-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6f421-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f421-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6f421-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6f421-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f421-120">CommonParameters</span></span>
<span data-ttu-id="6f421-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f421-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f421-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f421-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f421-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f421-123">INPUTS</span></span>

## <span data-ttu-id="6f421-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f421-124">OUTPUTS</span></span>

## <span data-ttu-id="6f421-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f421-125">NOTES</span></span>

## <span data-ttu-id="6f421-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f421-126">RELATED LINKS</span></span>

[<span data-ttu-id="6f421-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6f421-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="6f421-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6f421-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="6f421-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="6f421-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


