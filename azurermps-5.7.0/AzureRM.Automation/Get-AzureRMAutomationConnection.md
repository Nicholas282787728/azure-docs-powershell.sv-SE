---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: 85d2e5d3044efe97eef2b4aa784d8767973682f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574451"
---
# <span data-ttu-id="3ef12-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3ef12-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="3ef12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ef12-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef12-103">Hämtar en automatiserings anslutning.</span><span class="sxs-lookup"><span data-stu-id="3ef12-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ef12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ef12-104">SYNTAX</span></span>

### <span data-ttu-id="3ef12-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="3ef12-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ef12-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="3ef12-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ef12-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="3ef12-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ef12-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ef12-108">DESCRIPTION</span></span>
<span data-ttu-id="3ef12-109">Cmdleten **Get-AzureRmAutomationConnection** har en eller flera Azure Automation-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="3ef12-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="3ef12-110">Som standard hämtar denna cmdlet alla anslutningar.</span><span class="sxs-lookup"><span data-stu-id="3ef12-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="3ef12-111">Ange namnet på en anslutning för att få en specifik anslutning.</span><span class="sxs-lookup"><span data-stu-id="3ef12-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="3ef12-112">Ange namnet på anslutnings typen för att få alla anslutningar av en viss typ.</span><span class="sxs-lookup"><span data-stu-id="3ef12-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="3ef12-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ef12-113">EXAMPLES</span></span>

### <span data-ttu-id="3ef12-114">Exempel 1: Hämta alla anslutningar</span><span class="sxs-lookup"><span data-stu-id="3ef12-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3ef12-115">Det här kommandot får metadata för alla anslutningar i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3ef12-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3ef12-116">Exempel 2: Hämta alla anslutningar av en typ</span><span class="sxs-lookup"><span data-stu-id="3ef12-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="3ef12-117">Det här kommandot får metadata för anslutningar i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3ef12-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="3ef12-118">Det här kommandot får fram anslutningar av typen SqlServer.</span><span class="sxs-lookup"><span data-stu-id="3ef12-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="3ef12-119">Exempel 3: skaffa en anslutning</span><span class="sxs-lookup"><span data-stu-id="3ef12-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="3ef12-120">Det här kommandot får metadata för anslutningen med namnet ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="3ef12-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="3ef12-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ef12-121">PARAMETERS</span></span>

### <span data-ttu-id="3ef12-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ef12-122">-AutomationAccountName</span></span>
<span data-ttu-id="3ef12-123">Anger namnet på det Automation-konto som denna cmdlet ansluter till.</span><span class="sxs-lookup"><span data-stu-id="3ef12-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef12-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="3ef12-124">-ConnectionTypeName</span></span>
<span data-ttu-id="3ef12-125">Anger namnet på en Anslutnings typ för vilken denna cmdlet hämtar anslutningar.</span><span class="sxs-lookup"><span data-stu-id="3ef12-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef12-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef12-126">-DefaultProfile</span></span>
<span data-ttu-id="3ef12-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3ef12-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef12-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ef12-128">-Name</span></span>
<span data-ttu-id="3ef12-129">Anger namnet på en anslutning som hämtas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ef12-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef12-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef12-130">-ResourceGroupName</span></span>
<span data-ttu-id="3ef12-131">Anger namnet på en resurs grupp som denna cmdlet ansluter till.</span><span class="sxs-lookup"><span data-stu-id="3ef12-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef12-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef12-132">CommonParameters</span></span>
<span data-ttu-id="3ef12-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef12-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef12-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef12-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef12-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ef12-135">INPUTS</span></span>

### <span data-ttu-id="3ef12-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ef12-136">None</span></span>
<span data-ttu-id="3ef12-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3ef12-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ef12-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ef12-138">OUTPUTS</span></span>

### <span data-ttu-id="3ef12-139">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="3ef12-139">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="3ef12-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ef12-140">NOTES</span></span>

## <span data-ttu-id="3ef12-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ef12-141">RELATED LINKS</span></span>

[<span data-ttu-id="3ef12-142">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3ef12-142">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="3ef12-143">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3ef12-143">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


