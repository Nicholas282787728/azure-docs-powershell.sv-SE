---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099600"
---
# <span data-ttu-id="7feb5-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7feb5-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="7feb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7feb5-102">SYNOPSIS</span></span>

<span data-ttu-id="7feb5-103">Får en Azure Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="7feb5-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="7feb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7feb5-104">SYNTAX</span></span>

### <span data-ttu-id="7feb5-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="7feb5-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7feb5-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="7feb5-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7feb5-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="7feb5-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7feb5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7feb5-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7feb5-109">Cmdleten **Get-AzureAutomationConnection** har en eller flera Microsoft Azure Automation-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="7feb5-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="7feb5-110">Som standard returneras alla anslutningar.</span><span class="sxs-lookup"><span data-stu-id="7feb5-110">By default, all connections are returned.</span></span>
<span data-ttu-id="7feb5-111">Ange namnet på en specifik anslutning.</span><span class="sxs-lookup"><span data-stu-id="7feb5-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="7feb5-112">Om du vill hämta alla anslutningar av en viss typ anger du namnet på anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="7feb5-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="7feb5-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7feb5-113">EXAMPLES</span></span>

### <span data-ttu-id="7feb5-114">Exempel 1: Hämta alla anslutningar</span><span class="sxs-lookup"><span data-stu-id="7feb5-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7feb5-115">Det här kommandot får alla anslutningar i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7feb5-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7feb5-116">Exempel 2: Hämta alla anslutningar av en typ</span><span class="sxs-lookup"><span data-stu-id="7feb5-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="7feb5-117">Det här kommandot får alla Azure-anslutningar i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7feb5-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7feb5-118">Exempel 3: skaffa en anslutning</span><span class="sxs-lookup"><span data-stu-id="7feb5-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="7feb5-119">Det här kommandot får anslutningen som heter för anslutning.</span><span class="sxs-lookup"><span data-stu-id="7feb5-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="7feb5-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7feb5-120">PARAMETERS</span></span>

### <span data-ttu-id="7feb5-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7feb5-121">-AutomationAccountName</span></span>
<span data-ttu-id="7feb5-122">Anger namnet på det Automation-konto där anslutningen ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7feb5-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

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

### <span data-ttu-id="7feb5-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="7feb5-123">-ConnectionTypeName</span></span>
<span data-ttu-id="7feb5-124">Anger namnet på en Anslutnings typ för de anslutningar som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7feb5-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7feb5-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7feb5-125">-Name</span></span>
<span data-ttu-id="7feb5-126">Anger namnet på en anslutning som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7feb5-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7feb5-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="7feb5-127">-Profile</span></span>
<span data-ttu-id="7feb5-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7feb5-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7feb5-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7feb5-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7feb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7feb5-130">CommonParameters</span></span>
<span data-ttu-id="7feb5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7feb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7feb5-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7feb5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7feb5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7feb5-133">INPUTS</span></span>

## <span data-ttu-id="7feb5-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7feb5-134">OUTPUTS</span></span>

### <span data-ttu-id="7feb5-135">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="7feb5-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="7feb5-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7feb5-136">NOTES</span></span>

## <span data-ttu-id="7feb5-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7feb5-137">RELATED LINKS</span></span>

[<span data-ttu-id="7feb5-138">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7feb5-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="7feb5-139">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7feb5-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="7feb5-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="7feb5-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


