---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754803"
---
# <span data-ttu-id="1162d-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1162d-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="1162d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1162d-102">SYNOPSIS</span></span>
<span data-ttu-id="1162d-103">Skapar en Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="1162d-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="1162d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1162d-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1162d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1162d-105">DESCRIPTION</span></span>
<span data-ttu-id="1162d-106">Cmdleten **New-AzAutomationConnection** skapar en anslutning i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1162d-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="1162d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1162d-107">EXAMPLES</span></span>

### <span data-ttu-id="1162d-108">Exempel 1: skapa en anslutning</span><span class="sxs-lookup"><span data-stu-id="1162d-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="1162d-109">Det första kommandot tilldelar en hash-tabell med fält värden till $FieldValue variabel.</span><span class="sxs-lookup"><span data-stu-id="1162d-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="1162d-110">Det andra kommandot skapar en Azure-anslutning med namnet Connection12 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="1162d-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="1162d-111">Kommandot använder kopplings fält värden i $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="1162d-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="1162d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1162d-112">PARAMETERS</span></span>

### <span data-ttu-id="1162d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1162d-113">-AutomationAccountName</span></span>
<span data-ttu-id="1162d-114">Anger namnet på det Automation-konto som den här cmdleten skapar en anslutning för.</span><span class="sxs-lookup"><span data-stu-id="1162d-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1162d-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="1162d-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="1162d-116">Anger en hash-tabell som innehåller par av nycklar och värden.</span><span class="sxs-lookup"><span data-stu-id="1162d-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="1162d-117">Nycklarna representerar anslutnings fälten för den angivna anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="1162d-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="1162d-118">Värdena representerar de specifika värdena för varje anslutnings fält för anslutnings instansen.</span><span class="sxs-lookup"><span data-stu-id="1162d-118">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1162d-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="1162d-119">-ConnectionTypeName</span></span>
<span data-ttu-id="1162d-120">Anger namnet på anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="1162d-120">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1162d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1162d-121">-DefaultProfile</span></span>
<span data-ttu-id="1162d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1162d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1162d-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1162d-123">-Description</span></span>
<span data-ttu-id="1162d-124">Anger en beskrivning för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="1162d-124">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1162d-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="1162d-125">-Name</span></span>
<span data-ttu-id="1162d-126">Anger ett namn för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="1162d-126">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1162d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1162d-127">-ResourceGroupName</span></span>
<span data-ttu-id="1162d-128">Anger namnet på den resurs grupp som den här cmdleten skapar en anslutning för.</span><span class="sxs-lookup"><span data-stu-id="1162d-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1162d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1162d-129">CommonParameters</span></span>
<span data-ttu-id="1162d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1162d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1162d-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1162d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1162d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1162d-132">INPUTS</span></span>

### <span data-ttu-id="1162d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1162d-133">System.String</span></span>

### <span data-ttu-id="1162d-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="1162d-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="1162d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1162d-135">OUTPUTS</span></span>

### <span data-ttu-id="1162d-136">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="1162d-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="1162d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1162d-137">NOTES</span></span>

## <span data-ttu-id="1162d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1162d-138">RELATED LINKS</span></span>

[<span data-ttu-id="1162d-139">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1162d-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="1162d-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1162d-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


