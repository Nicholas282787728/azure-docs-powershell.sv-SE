---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573792"
---
# <span data-ttu-id="975c2-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="975c2-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="975c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="975c2-102">SYNOPSIS</span></span>
<span data-ttu-id="975c2-103">Ändrar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="975c2-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="975c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="975c2-104">SYNTAX</span></span>

### <span data-ttu-id="975c2-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="975c2-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975c2-106">Inaktivera säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="975c2-106">Disable Backup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="975c2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="975c2-107">DESCRIPTION</span></span>
<span data-ttu-id="975c2-108">Set-AzureRmAnalysisServicesServer cmdlet ändrar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="975c2-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="975c2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="975c2-109">EXAMPLES</span></span>

### <span data-ttu-id="975c2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="975c2-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="975c2-111">Ändrar den server som heter testserver i resourcegroup testgroup för att ställa in taggarna som KEY1: värde1 and key2: värde2 och Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="975c2-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="975c2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="975c2-112">PARAMETERS</span></span>

### <span data-ttu-id="975c2-113">-Administratör</span><span class="sxs-lookup"><span data-stu-id="975c2-113">-Administrator</span></span>
<span data-ttu-id="975c2-114">En sträng som representerar en kommaseparerad lista över användare eller grupper som ska anges som administratörer på servern.</span><span class="sxs-lookup"><span data-stu-id="975c2-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="975c2-115">Användare eller grupper måste ange UPN-format, t. ex. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="975c2-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="975c2-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="975c2-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="975c2-117">URI för BLOB-behållare för säkerhets kopiering av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="975c2-117">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="975c2-118">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="975c2-118">-DisableBackup</span></span>
<span data-ttu-id="975c2-119">Växeln för att inaktivera reserv-BLOB-containern.</span><span class="sxs-lookup"><span data-stu-id="975c2-119">The switch to disable backup blob container.</span></span>
<span data-ttu-id="975c2-120">För att återaktivera reserv-BLOB-behållaren ska du ange reserv-URI: n för BLOB-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="975c2-120">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="975c2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="975c2-121">-Name</span></span>
<span data-ttu-id="975c2-122">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="975c2-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="975c2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="975c2-123">-PassThru</span></span>
<span data-ttu-id="975c2-124">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="975c2-124">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="975c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="975c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="975c2-126">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="975c2-126">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="975c2-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="975c2-127">-Sku</span></span>
<span data-ttu-id="975c2-128">Namnet på SKU för servern.</span><span class="sxs-lookup"><span data-stu-id="975c2-128">The name of the Sku for the server.</span></span>
<span data-ttu-id="975c2-129">De värden som stöds är 0 ', ' 1 ', är 2 ', är 4 ' för standard nivån; "B1", "B2" för bas nivån och "d" för utvecklings nivån.</span><span class="sxs-lookup"><span data-stu-id="975c2-129">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="975c2-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="975c2-130">-Tag</span></span>
<span data-ttu-id="975c2-131">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="975c2-131">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="975c2-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="975c2-132">-Confirm</span></span>
<span data-ttu-id="975c2-133">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="975c2-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="975c2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="975c2-134">-WhatIf</span></span>
<span data-ttu-id="975c2-135">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="975c2-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="975c2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975c2-136">-DefaultProfile</span></span>
<span data-ttu-id="975c2-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="975c2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="975c2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975c2-138">CommonParameters</span></span>
<span data-ttu-id="975c2-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="975c2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975c2-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="975c2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975c2-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="975c2-141">INPUTS</span></span>

## <span data-ttu-id="975c2-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="975c2-142">OUTPUTS</span></span>

### <span data-ttu-id="975c2-143">Microsoft. Azure. Management. Analysis. Models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="975c2-143">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="975c2-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="975c2-144">NOTES</span></span>
<span data-ttu-id="975c2-145">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="975c2-145">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="975c2-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="975c2-146">RELATED LINKS</span></span>

[<span data-ttu-id="975c2-147">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="975c2-147">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="975c2-148">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="975c2-148">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
