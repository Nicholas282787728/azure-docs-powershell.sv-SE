---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 218ba8565ebf856a85b6a4b5b538c696d236fd82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758239"
---
# <span data-ttu-id="289ab-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="289ab-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="289ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="289ab-102">SYNOPSIS</span></span>
<span data-ttu-id="289ab-103">Skapar en ny Analysis Services-server</span><span class="sxs-lookup"><span data-stu-id="289ab-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="289ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="289ab-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="289ab-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="289ab-105">DESCRIPTION</span></span>
<span data-ttu-id="289ab-106">New-AzureRmAnalysisServicesServer-cmdleten skapar en ny Analysis Services-server</span><span class="sxs-lookup"><span data-stu-id="289ab-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="289ab-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="289ab-107">EXAMPLES</span></span>

### <span data-ttu-id="289ab-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="289ab-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="289ab-109">Skapar en server med namnet testserver i Azure-regionen West-US och i resurs grupp testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="289ab-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="289ab-110">SKU-nivån för servern blir S1.</span><span class="sxs-lookup"><span data-stu-id="289ab-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="289ab-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="289ab-111">PARAMETERS</span></span>

### <span data-ttu-id="289ab-112">-Administratör</span><span class="sxs-lookup"><span data-stu-id="289ab-112">-Administrator</span></span>
<span data-ttu-id="289ab-113">En sträng som representerar en kommaseparerad lista över användare eller grupper som ska anges som administratörer på servern.</span><span class="sxs-lookup"><span data-stu-id="289ab-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="289ab-114">Användare eller grupper måste ange UPN-format, t. ex. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="289ab-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="289ab-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="289ab-116">URI för BLOB-behållare för säkerhets kopiering av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="289ab-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289ab-117">-DefaultProfile</span></span>
<span data-ttu-id="289ab-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="289ab-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="289ab-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="289ab-119">-Location</span></span>
<span data-ttu-id="289ab-120">Azure-regionen där Analysis Services-servern finns</span><span class="sxs-lookup"><span data-stu-id="289ab-120">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="289ab-121">-Name</span></span>
<span data-ttu-id="289ab-122">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="289ab-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="289ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="289ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="289ab-124">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="289ab-124">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="289ab-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="289ab-125">-Sku</span></span>
<span data-ttu-id="289ab-126">Namnet på SKU för servern.</span><span class="sxs-lookup"><span data-stu-id="289ab-126">The name of the Sku for the server.</span></span>
<span data-ttu-id="289ab-127">De värden som stöds är 0 ', ' 1 ', är 2 ', är 4 ' för standard nivån; "B1", "B2" för bas nivån och "d" för utvecklings nivån.</span><span class="sxs-lookup"><span data-stu-id="289ab-127">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="289ab-128">-Tag</span></span>
<span data-ttu-id="289ab-129">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="289ab-129">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-130">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="289ab-130">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="289ab-131">Skrivskyddat antal repliker för en Analysis Service-server</span><span class="sxs-lookup"><span data-stu-id="289ab-131">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-132">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="289ab-132">-DefaultConnectionMode</span></span>
<span data-ttu-id="289ab-133">Standard anslutnings läge för en Analysis Service-server</span><span class="sxs-lookup"><span data-stu-id="289ab-133">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-134">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="289ab-134">-FirewallConfig</span></span>
<span data-ttu-id="289ab-135">Brand Väggs konfiguration för en analys Server</span><span class="sxs-lookup"><span data-stu-id="289ab-135">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="289ab-136">-Confirm</span></span>
<span data-ttu-id="289ab-137">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="289ab-137">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="289ab-138">-WhatIf</span></span>
<span data-ttu-id="289ab-139">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="289ab-139">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289ab-140">CommonParameters</span></span>
<span data-ttu-id="289ab-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="289ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289ab-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="289ab-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289ab-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="289ab-143">INPUTS</span></span>

### <span data-ttu-id="289ab-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="289ab-144">None</span></span>
<span data-ttu-id="289ab-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="289ab-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="289ab-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="289ab-146">OUTPUTS</span></span>

### <span data-ttu-id="289ab-147">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="289ab-147">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="289ab-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="289ab-148">NOTES</span></span>
<span data-ttu-id="289ab-149">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="289ab-149">Alias: New-AzureAs</span></span>

## <span data-ttu-id="289ab-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="289ab-150">RELATED LINKS</span></span>

[<span data-ttu-id="289ab-151">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="289ab-151">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="289ab-152">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="289ab-152">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
