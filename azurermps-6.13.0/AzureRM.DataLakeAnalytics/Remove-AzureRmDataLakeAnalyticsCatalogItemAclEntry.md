---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: e97876377e8ea96dc106277991bcc05fec5f3759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575237"
---
# <span data-ttu-id="036eb-101">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="036eb-101">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="036eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="036eb-102">SYNOPSIS</span></span>
<span data-ttu-id="036eb-103">Tar bort en post från en ACL för en katalog eller ett katalog objekt i data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="036eb-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="036eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="036eb-104">SYNTAX</span></span>

### <span data-ttu-id="036eb-105">RemoveCatalogAclEntryForUser (standard)</span><span class="sxs-lookup"><span data-stu-id="036eb-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036eb-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="036eb-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036eb-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="036eb-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036eb-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="036eb-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="036eb-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="036eb-109">DESCRIPTION</span></span>
<span data-ttu-id="036eb-110">Cmdleten **Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry** tar bort en post (ACE) från åtkomst kontrol listan (ACL) för en katalog eller katalog objekt i data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="036eb-110">The **Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="036eb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="036eb-111">EXAMPLES</span></span>

### <span data-ttu-id="036eb-112">Exempel 1: ta bort användarens ACL för en katalog</span><span class="sxs-lookup"><span data-stu-id="036eb-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="036eb-113">Det här kommandot tar bort katalog-ACL för Patti Nilsson till contosoadla-kontot.</span><span class="sxs-lookup"><span data-stu-id="036eb-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="036eb-114">Exempel 2: ta bort en användares ACL för en databas</span><span class="sxs-lookup"><span data-stu-id="036eb-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="036eb-115">Det här kommandot tar bort databasens ACL för Patti Nilsson till contosoadla-kontot.</span><span class="sxs-lookup"><span data-stu-id="036eb-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="036eb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="036eb-116">PARAMETERS</span></span>

### <span data-ttu-id="036eb-117">-Konto</span><span class="sxs-lookup"><span data-stu-id="036eb-117">-Account</span></span>
<span data-ttu-id="036eb-118">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="036eb-118">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036eb-119">-DefaultProfile</span></span>
<span data-ttu-id="036eb-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="036eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="036eb-121">-Grupp</span><span class="sxs-lookup"><span data-stu-id="036eb-121">-Group</span></span>
<span data-ttu-id="036eb-122">Ta bort ACL-förteckning för grupp.</span><span class="sxs-lookup"><span data-stu-id="036eb-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="036eb-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="036eb-123">-ItemType</span></span>
<span data-ttu-id="036eb-124">Anger typen av katalog eller katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="036eb-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="036eb-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="036eb-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="036eb-126">Katalogisering</span><span class="sxs-lookup"><span data-stu-id="036eb-126">Catalog</span></span>
- <span data-ttu-id="036eb-127">Databas</span><span class="sxs-lookup"><span data-stu-id="036eb-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036eb-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="036eb-128">-ObjectId</span></span>
<span data-ttu-id="036eb-129">Identiteten för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="036eb-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036eb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="036eb-130">-PassThru</span></span>
<span data-ttu-id="036eb-131">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="036eb-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="036eb-132">-Path</span><span class="sxs-lookup"><span data-stu-id="036eb-132">-Path</span></span>
<span data-ttu-id="036eb-133">Anger sökvägen till data Lake Analytics för en katalog eller katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="036eb-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="036eb-134">Delar av sökvägen ska avgränsas med en punkt (.).</span><span class="sxs-lookup"><span data-stu-id="036eb-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036eb-135">-Användare</span><span class="sxs-lookup"><span data-stu-id="036eb-135">-User</span></span>
<span data-ttu-id="036eb-136">Ta bort ACL-förteckning för användare.</span><span class="sxs-lookup"><span data-stu-id="036eb-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="036eb-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="036eb-137">-Confirm</span></span>
<span data-ttu-id="036eb-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="036eb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="036eb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="036eb-139">-WhatIf</span></span>
<span data-ttu-id="036eb-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="036eb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="036eb-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="036eb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="036eb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036eb-142">CommonParameters</span></span>
<span data-ttu-id="036eb-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="036eb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036eb-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="036eb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036eb-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="036eb-145">INPUTS</span></span>

### <span data-ttu-id="036eb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="036eb-146">System.String</span></span>

### <span data-ttu-id="036eb-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="036eb-147">System.Guid</span></span>

### <span data-ttu-id="036eb-148">Microsoft. Azure. commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="036eb-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="036eb-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="036eb-149">OUTPUTS</span></span>

### <span data-ttu-id="036eb-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="036eb-150">System.Boolean</span></span>

## <span data-ttu-id="036eb-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="036eb-151">NOTES</span></span>

## <span data-ttu-id="036eb-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="036eb-152">RELATED LINKS</span></span>

[<span data-ttu-id="036eb-153">U-SQL erbjuder nu åtkomst kontroll på databas nivå</span><span class="sxs-lookup"><span data-stu-id="036eb-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="036eb-154">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="036eb-154">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="036eb-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="036eb-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
