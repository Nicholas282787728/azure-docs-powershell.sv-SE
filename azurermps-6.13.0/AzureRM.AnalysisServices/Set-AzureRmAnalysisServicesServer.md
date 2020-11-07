---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 30f5e7237f497f3d9f4208548b56ede72583f067
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756746"
---
# <span data-ttu-id="3cc13-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3cc13-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="3cc13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3cc13-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc13-103">Ändrar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="3cc13-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cc13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3cc13-104">SYNTAX</span></span>

### <span data-ttu-id="3cc13-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="3cc13-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc13-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="3cc13-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc13-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="3cc13-107">DisassociateGateway</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc13-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3cc13-108">DESCRIPTION</span></span>
<span data-ttu-id="3cc13-109">Set-AzureRmAnalysisServicesServer cmdlet ändrar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="3cc13-109">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="3cc13-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3cc13-110">EXAMPLES</span></span>

### <span data-ttu-id="3cc13-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3cc13-111">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="3cc13-112">Ändrar den server som heter testserver i resourcegroup testgroup för att ställa in taggarna som KEY1: värde1 and key2: värde2 och Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3cc13-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="3cc13-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3cc13-113">PARAMETERS</span></span>

### <span data-ttu-id="3cc13-114">-Administratör</span><span class="sxs-lookup"><span data-stu-id="3cc13-114">-Administrator</span></span>
<span data-ttu-id="3cc13-115">En sträng som representerar en kommaseparerad lista över användare eller grupper som ska anges som administratörer på servern.</span><span class="sxs-lookup"><span data-stu-id="3cc13-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="3cc13-116">Användare eller grupper måste ange UPN-format, t. ex. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3cc13-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="3cc13-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="3cc13-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="3cc13-118">URI för BLOB-behållare för säkerhets kopiering av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="3cc13-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="3cc13-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="3cc13-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="3cc13-120">Standard anslutnings läge för en Analysis Service-server</span><span class="sxs-lookup"><span data-stu-id="3cc13-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="3cc13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc13-121">-DefaultProfile</span></span>
<span data-ttu-id="3cc13-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc13-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cc13-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="3cc13-123">-DisableBackup</span></span>
<span data-ttu-id="3cc13-124">Växeln för att inaktivera reserv-BLOB-containern.</span><span class="sxs-lookup"><span data-stu-id="3cc13-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="3cc13-125">För att återaktivera reserv-BLOB-behållaren ska du ange reserv-URI: n för BLOB-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="3cc13-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="3cc13-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="3cc13-126">-DisassociateGateway</span></span>
<span data-ttu-id="3cc13-127">Avassociera Gateway-resursen från en analys Server</span><span class="sxs-lookup"><span data-stu-id="3cc13-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="3cc13-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="3cc13-128">-FirewallConfig</span></span>
<span data-ttu-id="3cc13-129">Brand Väggs konfiguration för en analys Server</span><span class="sxs-lookup"><span data-stu-id="3cc13-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="3cc13-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3cc13-130">-GatewayResourceId</span></span>
<span data-ttu-id="3cc13-131">Gateway-resurs-ID för assocaite till en analys Server</span><span class="sxs-lookup"><span data-stu-id="3cc13-131">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="3cc13-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="3cc13-132">-Name</span></span>
<span data-ttu-id="3cc13-133">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="3cc13-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="3cc13-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cc13-134">-PassThru</span></span>
<span data-ttu-id="3cc13-135">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="3cc13-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="3cc13-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3cc13-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="3cc13-137">Skrivskyddat antal repliker för en Analysis Service-server</span><span class="sxs-lookup"><span data-stu-id="3cc13-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="3cc13-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc13-138">-ResourceGroupName</span></span>
<span data-ttu-id="3cc13-139">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="3cc13-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="3cc13-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="3cc13-140">-Sku</span></span>
<span data-ttu-id="3cc13-141">Namnet på SKU för servern.</span><span class="sxs-lookup"><span data-stu-id="3cc13-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="3cc13-142">De värden som stöds är 0 ', ' 1 ', är 2 ', är 4 ' för standard nivån; "B1", "B2" för bas nivån och "d" för utvecklings nivån.</span><span class="sxs-lookup"><span data-stu-id="3cc13-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="3cc13-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3cc13-143">-Tag</span></span>
<span data-ttu-id="3cc13-144">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="3cc13-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="3cc13-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3cc13-145">-Confirm</span></span>
<span data-ttu-id="3cc13-146">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="3cc13-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3cc13-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc13-147">-WhatIf</span></span>
<span data-ttu-id="3cc13-148">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="3cc13-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3cc13-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc13-149">CommonParameters</span></span>
<span data-ttu-id="3cc13-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc13-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc13-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc13-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc13-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3cc13-152">INPUTS</span></span>

### <span data-ttu-id="3cc13-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc13-153">System.String</span></span>

### <span data-ttu-id="3cc13-154">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3cc13-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3cc13-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3cc13-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3cc13-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3cc13-156">System.Int32</span></span>

### <span data-ttu-id="3cc13-157">Microsoft. Azure. commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="3cc13-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="3cc13-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3cc13-158">OUTPUTS</span></span>

### <span data-ttu-id="3cc13-159">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3cc13-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="3cc13-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3cc13-160">NOTES</span></span>
<span data-ttu-id="3cc13-161">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="3cc13-161">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="3cc13-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3cc13-162">RELATED LINKS</span></span>

[<span data-ttu-id="3cc13-163">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3cc13-163">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="3cc13-164">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3cc13-164">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
