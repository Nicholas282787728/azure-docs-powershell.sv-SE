---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 1dc9546dd48285e1c2d6117578002d5aa523e5f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745888"
---
# <span data-ttu-id="d1cb9-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d1cb9-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d1cb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="d1cb9-103">Skapar en ny Analysis Services-server</span><span class="sxs-lookup"><span data-stu-id="d1cb9-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="d1cb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1cb9-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1cb9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="d1cb9-106">New-AzAnalysisServicesServer-cmdleten skapar en ny Analysis Services-server</span><span class="sxs-lookup"><span data-stu-id="d1cb9-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="d1cb9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1cb9-107">EXAMPLES</span></span>

### <span data-ttu-id="d1cb9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1cb9-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="d1cb9-109">Skapar en server med namnet testserver i Azure-regionen West-US och i resurs grupp testresourcegroup.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-109">Creates a server named testserver in the Azure region West-US and in resource group testresourcegroup.</span></span> <span data-ttu-id="d1cb9-110">SKU-nivån för servern blir S1.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="d1cb9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1cb9-111">PARAMETERS</span></span>

### <span data-ttu-id="d1cb9-112">-Administratör</span><span class="sxs-lookup"><span data-stu-id="d1cb9-112">-Administrator</span></span>
<span data-ttu-id="d1cb9-113">En sträng som representerar en kommaseparerad lista över användare eller grupper som ska anges som administratörer på servern.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="d1cb9-114">Användare eller grupper måste ange UPN-format, t. ex. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d1cb9-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb9-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="d1cb9-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="d1cb9-116">URI för BLOB-behållare för säkerhets kopiering av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="d1cb9-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb9-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="d1cb9-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="d1cb9-118">Standard anslutnings läge för en Analysis Service-server</span><span class="sxs-lookup"><span data-stu-id="d1cb9-118">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1cb9-119">-DefaultProfile</span></span>
<span data-ttu-id="d1cb9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1cb9-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="d1cb9-121">-FirewallConfig</span></span>
<span data-ttu-id="d1cb9-122">Brand Väggs konfiguration för en analys Server</span><span class="sxs-lookup"><span data-stu-id="d1cb9-122">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb9-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d1cb9-123">-GatewayResourceId</span></span>
<span data-ttu-id="d1cb9-124">Gateway-resurs-ID som associeras med en analys Server</span><span class="sxs-lookup"><span data-stu-id="d1cb9-124">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="d1cb9-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="d1cb9-125">-Location</span></span>
<span data-ttu-id="d1cb9-126">Azure-regionen där Analysis Services-servern finns</span><span class="sxs-lookup"><span data-stu-id="d1cb9-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="d1cb9-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1cb9-127">-Name</span></span>
<span data-ttu-id="d1cb9-128">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="d1cb9-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="d1cb9-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="d1cb9-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="d1cb9-130">Skrivskyddat antal repliker för en Analysis Service-server</span><span class="sxs-lookup"><span data-stu-id="d1cb9-130">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1cb9-131">-ResourceGroupName</span></span>
<span data-ttu-id="d1cb9-132">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="d1cb9-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="d1cb9-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="d1cb9-133">-Sku</span></span>
<span data-ttu-id="d1cb9-134">Namnet på SKU för servern.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="d1cb9-135">De värden som stöds är 0 ', ' 1 ', är 2 ', är 4 ' för standard nivån; "B1", "B2" för bas nivån och "d" för utvecklings nivån.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="d1cb9-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d1cb9-136">-Tag</span></span>
<span data-ttu-id="d1cb9-137">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb9-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1cb9-138">-Confirm</span></span>
<span data-ttu-id="d1cb9-139">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="d1cb9-139">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1cb9-140">-WhatIf</span></span>
<span data-ttu-id="d1cb9-141">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="d1cb9-141">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cb9-142">CommonParameters</span></span>
<span data-ttu-id="d1cb9-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cb9-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1cb9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cb9-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1cb9-145">INPUTS</span></span>

### <span data-ttu-id="d1cb9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d1cb9-146">System.String</span></span>

### <span data-ttu-id="d1cb9-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="d1cb9-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d1cb9-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d1cb9-148">System.Int32</span></span>

### <span data-ttu-id="d1cb9-149">Microsoft. Azure. commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="d1cb9-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="d1cb9-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1cb9-150">OUTPUTS</span></span>

### <span data-ttu-id="d1cb9-151">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d1cb9-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d1cb9-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1cb9-152">NOTES</span></span>
<span data-ttu-id="d1cb9-153">Alias: New-AzAs</span><span class="sxs-lookup"><span data-stu-id="d1cb9-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="d1cb9-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1cb9-154">RELATED LINKS</span></span>

[<span data-ttu-id="d1cb9-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d1cb9-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="d1cb9-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d1cb9-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
