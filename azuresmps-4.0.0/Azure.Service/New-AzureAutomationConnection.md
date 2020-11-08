---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099450"
---
# <span data-ttu-id="e8346-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e8346-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="e8346-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8346-102">SYNOPSIS</span></span>

<span data-ttu-id="e8346-103">Skapar en anslutning i Automation.</span><span class="sxs-lookup"><span data-stu-id="e8346-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="e8346-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8346-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8346-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8346-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e8346-106">Cmdleten **New-AzureAutomationConnection** skapar en anslutning i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e8346-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e8346-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8346-107">EXAMPLES</span></span>

## <span data-ttu-id="e8346-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8346-108">PARAMETERS</span></span>

### <span data-ttu-id="e8346-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8346-109">-AutomationAccountName</span></span>
<span data-ttu-id="e8346-110">Anger namnet på Automation-kontot som anslutningen sparas i.</span><span class="sxs-lookup"><span data-stu-id="e8346-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

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

### <span data-ttu-id="e8346-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="e8346-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="e8346-112">Anger en hash-tabell som innehåller par av nycklar och värden.</span><span class="sxs-lookup"><span data-stu-id="e8346-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="e8346-113">Nycklarna representerar anslutnings fälten i den angivna anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="e8346-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="e8346-114">Värdena representerar de specifika värden som ska lagras för varje anslutnings fält för anslutnings instansen.</span><span class="sxs-lookup"><span data-stu-id="e8346-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8346-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="e8346-115">-ConnectionTypeName</span></span>
<span data-ttu-id="e8346-116">Anger namnet på anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="e8346-116">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="e8346-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e8346-117">-Description</span></span>
<span data-ttu-id="e8346-118">Anger en beskrivning av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="e8346-118">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="e8346-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8346-119">-Name</span></span>
<span data-ttu-id="e8346-120">Anger ett namn för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="e8346-120">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="e8346-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="e8346-121">-Profile</span></span>
<span data-ttu-id="e8346-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e8346-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8346-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e8346-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e8346-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8346-124">CommonParameters</span></span>
<span data-ttu-id="e8346-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8346-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8346-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8346-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8346-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8346-127">INPUTS</span></span>

## <span data-ttu-id="e8346-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8346-128">OUTPUTS</span></span>

### <span data-ttu-id="e8346-129">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="e8346-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="e8346-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8346-130">NOTES</span></span>

## <span data-ttu-id="e8346-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8346-131">RELATED LINKS</span></span>

[<span data-ttu-id="e8346-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e8346-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="e8346-133">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e8346-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="e8346-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="e8346-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


