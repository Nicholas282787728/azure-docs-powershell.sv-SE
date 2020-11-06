---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: 2964102dbb3f12b797d3d551f7bd4097ca8836a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578544"
---
# <span data-ttu-id="a9fb9-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a9fb9-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="a9fb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fb9-103">Skapar en Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9fb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9fb9-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9fb9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9fb9-105">DESCRIPTION</span></span>
<span data-ttu-id="a9fb9-106">Cmdleten **New-AzureRmAutomationConnection** skapar en anslutning i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="a9fb9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9fb9-107">EXAMPLES</span></span>

### <span data-ttu-id="a9fb9-108">Exempel 1: skapa en anslutning</span><span class="sxs-lookup"><span data-stu-id="a9fb9-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a9fb9-109">Det första kommandot tilldelar en hash-tabell med fält värden till $FieldValue variabel.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>

<span data-ttu-id="a9fb9-110">Det andra kommandot skapar en Azure-anslutning med namnet Connection12 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a9fb9-111">Kommandot använder kopplings fält värden i $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="a9fb9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9fb9-112">PARAMETERS</span></span>

### <span data-ttu-id="a9fb9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9fb9-113">-AutomationAccountName</span></span>
<span data-ttu-id="a9fb9-114">Anger namnet på det Automation-konto som den här cmdleten skapar en anslutning för.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="a9fb9-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="a9fb9-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="a9fb9-116">Anger en hash-tabell som innehåller par av nycklar och värden.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="a9fb9-117">Nycklarna representerar anslutnings fälten för den angivna anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="a9fb9-118">Värdena representerar de specifika värdena för varje anslutnings fält för anslutnings instansen.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="a9fb9-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="a9fb9-119">-ConnectionTypeName</span></span>
<span data-ttu-id="a9fb9-120">Anger namnet på anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="a9fb9-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a9fb9-121">-Description</span></span>
<span data-ttu-id="a9fb9-122">Anger en beskrivning för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-122">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="a9fb9-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9fb9-123">-Name</span></span>
<span data-ttu-id="a9fb9-124">Anger ett namn för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-124">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="a9fb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9fb9-126">Anger namnet på den resurs grupp som den här cmdleten skapar en anslutning för.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-126">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="a9fb9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fb9-127">-DefaultProfile</span></span>
<span data-ttu-id="a9fb9-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fb9-129">CommonParameters</span></span>
<span data-ttu-id="a9fb9-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fb9-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9fb9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fb9-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9fb9-132">INPUTS</span></span>

## <span data-ttu-id="a9fb9-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9fb9-133">OUTPUTS</span></span>

### <span data-ttu-id="a9fb9-134">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="a9fb9-134">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="a9fb9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9fb9-135">NOTES</span></span>

## <span data-ttu-id="a9fb9-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9fb9-136">RELATED LINKS</span></span>

[<span data-ttu-id="a9fb9-137">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a9fb9-137">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="a9fb9-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a9fb9-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


