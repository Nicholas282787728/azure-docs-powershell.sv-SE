---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 267c18ea4abf87936c47629eca523b254b411240
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754867"
---
# <span data-ttu-id="7dd65-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7dd65-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="7dd65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7dd65-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd65-103">Hämtar en automatiserings anslutning.</span><span class="sxs-lookup"><span data-stu-id="7dd65-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="7dd65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7dd65-104">SYNTAX</span></span>

### <span data-ttu-id="7dd65-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="7dd65-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dd65-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="7dd65-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dd65-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="7dd65-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dd65-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7dd65-108">DESCRIPTION</span></span>
<span data-ttu-id="7dd65-109">Cmdleten **Get-AzAutomationConnection** har en eller flera Azure Automation-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="7dd65-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="7dd65-110">Som standard hämtar denna cmdlet alla anslutningar.</span><span class="sxs-lookup"><span data-stu-id="7dd65-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="7dd65-111">Ange namnet på en anslutning för att få en specifik anslutning.</span><span class="sxs-lookup"><span data-stu-id="7dd65-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="7dd65-112">Ange namnet på anslutnings typen för att få alla anslutningar av en viss typ.</span><span class="sxs-lookup"><span data-stu-id="7dd65-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="7dd65-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7dd65-113">EXAMPLES</span></span>

### <span data-ttu-id="7dd65-114">Exempel 1: Hämta alla anslutningar</span><span class="sxs-lookup"><span data-stu-id="7dd65-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7dd65-115">Det här kommandot får metadata för alla anslutningar i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7dd65-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7dd65-116">Exempel 2: Hämta alla anslutningar av en typ</span><span class="sxs-lookup"><span data-stu-id="7dd65-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="7dd65-117">Det här kommandot får metadata för anslutningar i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7dd65-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="7dd65-118">Det här kommandot får fram anslutningar av typen SqlServer.</span><span class="sxs-lookup"><span data-stu-id="7dd65-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="7dd65-119">Exempel 3: skaffa en anslutning</span><span class="sxs-lookup"><span data-stu-id="7dd65-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="7dd65-120">Det här kommandot får metadata för anslutningen med namnet ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="7dd65-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="7dd65-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7dd65-121">PARAMETERS</span></span>

### <span data-ttu-id="7dd65-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7dd65-122">-AutomationAccountName</span></span>
<span data-ttu-id="7dd65-123">Anger namnet på det Automation-konto som denna cmdlet ansluter till.</span><span class="sxs-lookup"><span data-stu-id="7dd65-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="7dd65-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="7dd65-124">-ConnectionTypeName</span></span>
<span data-ttu-id="7dd65-125">Anger namnet på en Anslutnings typ för vilken denna cmdlet hämtar anslutningar.</span><span class="sxs-lookup"><span data-stu-id="7dd65-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd65-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd65-126">-DefaultProfile</span></span>
<span data-ttu-id="7dd65-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7dd65-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dd65-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="7dd65-128">-Name</span></span>
<span data-ttu-id="7dd65-129">Anger namnet på en anslutning som hämtas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dd65-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd65-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dd65-130">-ResourceGroupName</span></span>
<span data-ttu-id="7dd65-131">Anger namnet på en resurs grupp som denna cmdlet ansluter till.</span><span class="sxs-lookup"><span data-stu-id="7dd65-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="7dd65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd65-132">CommonParameters</span></span>
<span data-ttu-id="7dd65-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd65-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd65-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd65-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7dd65-135">INPUTS</span></span>

### <span data-ttu-id="7dd65-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7dd65-136">System.String</span></span>

## <span data-ttu-id="7dd65-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7dd65-137">OUTPUTS</span></span>

### <span data-ttu-id="7dd65-138">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="7dd65-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="7dd65-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7dd65-139">NOTES</span></span>

## <span data-ttu-id="7dd65-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7dd65-140">RELATED LINKS</span></span>

[<span data-ttu-id="7dd65-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7dd65-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="7dd65-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7dd65-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


