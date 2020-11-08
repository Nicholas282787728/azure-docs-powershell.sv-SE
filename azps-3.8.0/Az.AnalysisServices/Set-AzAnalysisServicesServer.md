---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: d13ffe73ada97ba68825beeb1769572767b3561a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089691"
---
# <span data-ttu-id="e3e51-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e3e51-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="e3e51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3e51-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e51-103">Ändrar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="e3e51-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="e3e51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3e51-104">SYNTAX</span></span>

### <span data-ttu-id="e3e51-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="e3e51-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e51-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="e3e51-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e51-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="e3e51-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e51-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3e51-108">DESCRIPTION</span></span>
<span data-ttu-id="e3e51-109">Set-AzAnalysisServicesServer cmdlet ändrar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="e3e51-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="e3e51-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3e51-110">EXAMPLES</span></span>

### <span data-ttu-id="e3e51-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3e51-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="e3e51-112">Ändrar den server som heter testserver i resourcegroup testgroup för att ställa in taggarna som KEY1: värde1 and key2: värde2 och Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="e3e51-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="e3e51-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3e51-113">PARAMETERS</span></span>

### <span data-ttu-id="e3e51-114">-Administratör</span><span class="sxs-lookup"><span data-stu-id="e3e51-114">-Administrator</span></span>
<span data-ttu-id="e3e51-115">En sträng som representerar en kommaseparerad lista över användare eller grupper som ska anges som administratörer på servern.</span><span class="sxs-lookup"><span data-stu-id="e3e51-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="e3e51-116">Användare eller grupper måste ange UPN-format, t. ex. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="e3e51-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="e3e51-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="e3e51-118">URI för BLOB-behållare för säkerhets kopiering av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="e3e51-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="e3e51-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="e3e51-120">Standard anslutnings läge för en Analysis Service-server</span><span class="sxs-lookup"><span data-stu-id="e3e51-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="e3e51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e51-121">-DefaultProfile</span></span>
<span data-ttu-id="e3e51-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3e51-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3e51-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="e3e51-123">-DisableBackup</span></span>
<span data-ttu-id="e3e51-124">Växeln för att inaktivera reserv-BLOB-containern.</span><span class="sxs-lookup"><span data-stu-id="e3e51-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="e3e51-125">För att återaktivera reserv-BLOB-behållaren ska du ange reserv-URI: n för BLOB-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="e3e51-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="e3e51-126">-DisassociateGateway</span></span>
<span data-ttu-id="e3e51-127">Avassociera Gateway-resursen från en analys Server</span><span class="sxs-lookup"><span data-stu-id="e3e51-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="e3e51-128">-FirewallConfig</span></span>
<span data-ttu-id="e3e51-129">Brand Väggs konfiguration för en analys Server</span><span class="sxs-lookup"><span data-stu-id="e3e51-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="e3e51-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e51-130">-GatewayResourceId</span></span>
<span data-ttu-id="e3e51-131">Gateway-resurs-ID som associeras med en analys Server</span><span class="sxs-lookup"><span data-stu-id="e3e51-131">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3e51-132">-Name</span></span>
<span data-ttu-id="e3e51-133">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="e3e51-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="e3e51-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3e51-134">-PassThru</span></span>
<span data-ttu-id="e3e51-135">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="e3e51-135">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="e3e51-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="e3e51-137">Skrivskyddat antal repliker för en Analysis Service-server</span><span class="sxs-lookup"><span data-stu-id="e3e51-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="e3e51-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e51-138">-ResourceGroupName</span></span>
<span data-ttu-id="e3e51-139">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="e3e51-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="e3e51-140">-Sku</span></span>
<span data-ttu-id="e3e51-141">Namnet på SKU för servern.</span><span class="sxs-lookup"><span data-stu-id="e3e51-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="e3e51-142">De värden som stöds är 0 ', ' 1 ', är 2 ', är 4 ' för standard nivån; "B1", "B2" för bas nivån och "d" för utvecklings nivån.</span><span class="sxs-lookup"><span data-stu-id="e3e51-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e3e51-143">-Tag</span></span>
<span data-ttu-id="e3e51-144">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="e3e51-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e51-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3e51-145">-Confirm</span></span>
<span data-ttu-id="e3e51-146">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="e3e51-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e3e51-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e51-147">-WhatIf</span></span>
<span data-ttu-id="e3e51-148">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="e3e51-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e3e51-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e51-149">CommonParameters</span></span>
<span data-ttu-id="e3e51-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3e51-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e51-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3e51-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e51-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3e51-152">INPUTS</span></span>

### <span data-ttu-id="e3e51-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e3e51-153">System.String</span></span>

### <span data-ttu-id="e3e51-154">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="e3e51-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e3e51-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e3e51-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e3e51-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e3e51-156">System.Int32</span></span>

### <span data-ttu-id="e3e51-157">Microsoft. Azure. commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="e3e51-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="e3e51-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3e51-158">OUTPUTS</span></span>

### <span data-ttu-id="e3e51-159">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e3e51-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="e3e51-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3e51-160">NOTES</span></span>
<span data-ttu-id="e3e51-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="e3e51-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="e3e51-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3e51-162">RELATED LINKS</span></span>

[<span data-ttu-id="e3e51-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e3e51-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="e3e51-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e3e51-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
