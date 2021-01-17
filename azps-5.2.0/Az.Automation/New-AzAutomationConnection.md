---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418528"
---
# <span data-ttu-id="01e12-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="01e12-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="01e12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01e12-102">SYNOPSIS</span></span>
<span data-ttu-id="01e12-103">Skapar en Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="01e12-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="01e12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01e12-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01e12-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01e12-105">DESCRIPTION</span></span>
<span data-ttu-id="01e12-106">Cmdleten **New-AzAutomationConnection** skapar en anslutning i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="01e12-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="01e12-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01e12-107">EXAMPLES</span></span>

### <span data-ttu-id="01e12-108">Exempel 1: skapa en anslutning för ConnectionTypeName = Azure</span><span class="sxs-lookup"><span data-stu-id="01e12-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="01e12-109">Det första kommandot tilldelar en hash-tabell med fält värden till $FieldValue variabel.</span><span class="sxs-lookup"><span data-stu-id="01e12-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="01e12-110">Det andra kommandot skapar en Azure-anslutning med namnet Connection12 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="01e12-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="01e12-111">Kommandot använder kopplings fält värden i $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="01e12-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="01e12-112">Exempel 2: skapa en anslutning för ConnectionTypeName = AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="01e12-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="01e12-113">Kommandot skapar en Azure-anslutning med namnet Connection13 i Automation-kontot med namnet AutomationAccount01 med $RunAsAccountConnectionFieldValues och ConnectionTypeName = AzureServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="01e12-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="01e12-114">Denna ConnectionTypeName = AzureServicePrincipal används främst för Azure kör som-konto.</span><span class="sxs-lookup"><span data-stu-id="01e12-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="01e12-115">Exempel 3: skapa en anslutning för ConnectionTypeName = AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="01e12-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="01e12-116">Kommandot skapar en Azure-anslutning med namnet Connection14 i Automation-kontot med namnet AutomationAccount01 med $ClassicRunAsAccountConnectionFieldValues och ConnectionTypeName = AzureClassicCertificate.</span><span class="sxs-lookup"><span data-stu-id="01e12-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="01e12-117">Denna ConnectionTypeName = AzureClassicCertificate används främst för det klassiska kör som-kontot för Azure.</span><span class="sxs-lookup"><span data-stu-id="01e12-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="01e12-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01e12-118">PARAMETERS</span></span>

### <span data-ttu-id="01e12-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="01e12-119">-AutomationAccountName</span></span>
<span data-ttu-id="01e12-120">Anger namnet på det Automation-konto som den här cmdleten skapar en anslutning för.</span><span class="sxs-lookup"><span data-stu-id="01e12-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="01e12-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="01e12-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="01e12-122">Anger en hash-tabell som innehåller par av nycklar och värden.</span><span class="sxs-lookup"><span data-stu-id="01e12-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="01e12-123">Nycklarna representerar anslutnings fälten för den angivna anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="01e12-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="01e12-124">Värdena representerar de specifika värdena för varje anslutnings fält för anslutnings instansen.</span><span class="sxs-lookup"><span data-stu-id="01e12-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="01e12-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="01e12-125">-ConnectionTypeName</span></span>
<span data-ttu-id="01e12-126">Anger namnet på anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="01e12-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="01e12-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e12-127">-DefaultProfile</span></span>
<span data-ttu-id="01e12-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="01e12-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01e12-129">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="01e12-129">-Description</span></span>
<span data-ttu-id="01e12-130">Anger en beskrivning för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="01e12-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="01e12-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="01e12-131">-Name</span></span>
<span data-ttu-id="01e12-132">Anger ett namn för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="01e12-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="01e12-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e12-133">-ResourceGroupName</span></span>
<span data-ttu-id="01e12-134">Anger namnet på den resurs grupp som den här cmdleten skapar en anslutning för.</span><span class="sxs-lookup"><span data-stu-id="01e12-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="01e12-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e12-135">CommonParameters</span></span>
<span data-ttu-id="01e12-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e12-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e12-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e12-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e12-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01e12-138">INPUTS</span></span>

### <span data-ttu-id="01e12-139">System. String</span><span class="sxs-lookup"><span data-stu-id="01e12-139">System.String</span></span>

### <span data-ttu-id="01e12-140">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="01e12-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="01e12-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01e12-141">OUTPUTS</span></span>

### <span data-ttu-id="01e12-142">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="01e12-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="01e12-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01e12-143">NOTES</span></span>

## <span data-ttu-id="01e12-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01e12-144">RELATED LINKS</span></span>

[<span data-ttu-id="01e12-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="01e12-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="01e12-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="01e12-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


