---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 349fe79bf3ff3bea0097542ee0189b5a1999bd35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757100"
---
# <span data-ttu-id="5ed46-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5ed46-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="5ed46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ed46-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed46-103">Hämtar en post i ACL för en katalog eller katalog objekt i data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5ed46-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ed46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ed46-104">SYNTAX</span></span>

### <span data-ttu-id="5ed46-105">GetCatalogAclEntry (standard)</span><span class="sxs-lookup"><span data-stu-id="5ed46-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ed46-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="5ed46-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ed46-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="5ed46-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ed46-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5ed46-108">GetCatalogItemAclEntry</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ed46-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="5ed46-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ed46-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="5ed46-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ed46-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ed46-111">DESCRIPTION</span></span>
<span data-ttu-id="5ed46-112">Cmdleten **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** hämtar en lista med poster (ACE) i ACL (Access Control List) för en katalog eller katalog objekt i data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5ed46-112">The **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="5ed46-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ed46-113">EXAMPLES</span></span>

### <span data-ttu-id="5ed46-114">Exempel 1: Hämta ACL för en katalog</span><span class="sxs-lookup"><span data-stu-id="5ed46-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="5ed46-115">Det här kommandot får ACL för katalogen för det angivna data Lake Analytics-kontot</span><span class="sxs-lookup"><span data-stu-id="5ed46-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="5ed46-116">Exempel 2: Hämta ACL-posten för användar ägare för en katalog</span><span class="sxs-lookup"><span data-stu-id="5ed46-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="5ed46-117">Det här kommandot får ACL-posten för användarens ägare för katalogen för det angivna data Lake Analytics-kontot</span><span class="sxs-lookup"><span data-stu-id="5ed46-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="5ed46-118">Exempel 3: Hämta ACL-posten för grupp ägare för en katalog</span><span class="sxs-lookup"><span data-stu-id="5ed46-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="5ed46-119">Det här kommandot får ACL-posten för grupp ägaren för katalogen för det angivna data Lake Analytics-kontot</span><span class="sxs-lookup"><span data-stu-id="5ed46-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="5ed46-120">Exempel 4: Hämta ACL för en databas</span><span class="sxs-lookup"><span data-stu-id="5ed46-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="5ed46-121">Det här kommandot får ACL för databasen för det angivna data Lake Analytics-kontot</span><span class="sxs-lookup"><span data-stu-id="5ed46-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="5ed46-122">Exempel 5: Hämta ACL-posten för användar ägare för en databas</span><span class="sxs-lookup"><span data-stu-id="5ed46-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="5ed46-123">Det här kommandot får ACL-posten för användarens ägare för databasen för det angivna data Lake Analytics-kontot</span><span class="sxs-lookup"><span data-stu-id="5ed46-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="5ed46-124">Exempel 6: Hämta ACL-posten för grupp ägare för en databas</span><span class="sxs-lookup"><span data-stu-id="5ed46-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="5ed46-125">Det här kommandot får ACL-posten för grupp ägaren för databasen för det angivna data Lake Analytics-kontot</span><span class="sxs-lookup"><span data-stu-id="5ed46-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="5ed46-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ed46-126">PARAMETERS</span></span>

### <span data-ttu-id="5ed46-127">-Konto</span><span class="sxs-lookup"><span data-stu-id="5ed46-127">-Account</span></span>
<span data-ttu-id="5ed46-128">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="5ed46-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5ed46-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed46-129">-DefaultProfile</span></span>
<span data-ttu-id="5ed46-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed46-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ed46-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="5ed46-131">-GroupOwner</span></span>
<span data-ttu-id="5ed46-132">Hämta ACL-förteckning för grupp ägare</span><span class="sxs-lookup"><span data-stu-id="5ed46-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed46-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="5ed46-133">-ItemType</span></span>
<span data-ttu-id="5ed46-134">Anger typen av katalog eller katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="5ed46-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="5ed46-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5ed46-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5ed46-136">Katalogisering</span><span class="sxs-lookup"><span data-stu-id="5ed46-136">Catalog</span></span>
- <span data-ttu-id="5ed46-137">Databas</span><span class="sxs-lookup"><span data-stu-id="5ed46-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed46-138">-Path</span><span class="sxs-lookup"><span data-stu-id="5ed46-138">-Path</span></span>
<span data-ttu-id="5ed46-139">Anger sökvägen till data Lake Analytics för en katalog eller katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="5ed46-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="5ed46-140">Delar av sökvägen ska avgränsas med en punkt (.).</span><span class="sxs-lookup"><span data-stu-id="5ed46-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed46-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="5ed46-141">-UserOwner</span></span>
<span data-ttu-id="5ed46-142">Hämta ACL-post för katalogen för användarens ägare.</span><span class="sxs-lookup"><span data-stu-id="5ed46-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed46-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed46-143">CommonParameters</span></span>
<span data-ttu-id="5ed46-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed46-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed46-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed46-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed46-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ed46-146">INPUTS</span></span>

### <span data-ttu-id="5ed46-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5ed46-147">System.String</span></span>

### <span data-ttu-id="5ed46-148">Microsoft. Azure. commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="5ed46-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="5ed46-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ed46-149">OUTPUTS</span></span>

### <span data-ttu-id="5ed46-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="5ed46-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="5ed46-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ed46-151">NOTES</span></span>

## <span data-ttu-id="5ed46-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ed46-152">RELATED LINKS</span></span>

[<span data-ttu-id="5ed46-153">U-SQL erbjuder nu åtkomst kontroll på databas nivå</span><span class="sxs-lookup"><span data-stu-id="5ed46-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="5ed46-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5ed46-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="5ed46-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5ed46-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
