---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: b728f53c34120fb0612f42491007c9d58998da0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757372"
---
# <span data-ttu-id="8ceb8-101">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8ceb8-101">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="8ceb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ceb8-102">SYNOPSIS</span></span>
<span data-ttu-id="8ceb8-103">Ändrar en post i ACL för en katalog eller katalog objekt i data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ceb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ceb8-104">SYNTAX</span></span>

### <span data-ttu-id="8ceb8-105">SetCatalogAclEntryForUser (standard)</span><span class="sxs-lookup"><span data-stu-id="8ceb8-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="8ceb8-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="8ceb8-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="8ceb8-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="8ceb8-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="8ceb8-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="8ceb8-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="8ceb8-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="8ceb8-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ceb8-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="8ceb8-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ceb8-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ceb8-115">DESCRIPTION</span></span>
<span data-ttu-id="8ceb8-116">Cmdleten **set-AzureRmDataLakeAnalyticsCatalogItemAclEntry** lägger till eller ändrar en post (ACE) i åtkomst kontrol listan (ACL) för en katalog eller katalog objekt i data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-116">The **Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="8ceb8-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ceb8-117">EXAMPLES</span></span>

### <span data-ttu-id="8ceb8-118">Exempel 1: ändra användar behörigheter för en katalog</span><span class="sxs-lookup"><span data-stu-id="8ceb8-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="8ceb8-119">Det här kommandot ändrar katalogens ACE för Patti Nilsson till Läs behörighet.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="8ceb8-120">Exempel 2: ändra användar behörigheter för en databas</span><span class="sxs-lookup"><span data-stu-id="8ceb8-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="8ceb8-121">Det här kommandot ändrar databasens ACE för Patti Nilsson till Läs behörighet.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="8ceb8-122">Exempel 3: ändra andra behörigheter för en katalog</span><span class="sxs-lookup"><span data-stu-id="8ceb8-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="8ceb8-123">Det här kommandot ändrar katalogens ACE för att få Läs behörighet.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="8ceb8-124">Exempel 4: ändra andra behörigheter för en databas</span><span class="sxs-lookup"><span data-stu-id="8ceb8-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="8ceb8-125">Exempel 5: ändra behörigheter för användar ägare för en katalog</span><span class="sxs-lookup"><span data-stu-id="8ceb8-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="8ceb8-126">Det här kommandot anger ägar behörigheten för kontot som ska läsas.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="8ceb8-127">Exempel 6: ändra behörigheter för användar ägare för en databas</span><span class="sxs-lookup"><span data-stu-id="8ceb8-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="8ceb8-128">Det här kommandot anger ägar behörighet för databasen att läsa.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="8ceb8-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ceb8-129">PARAMETERS</span></span>

### <span data-ttu-id="8ceb8-130">-Konto</span><span class="sxs-lookup"><span data-stu-id="8ceb8-130">-Account</span></span>
<span data-ttu-id="8ceb8-131">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8ceb8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ceb8-132">-DefaultProfile</span></span>
<span data-ttu-id="8ceb8-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ceb8-134">-Grupp</span><span class="sxs-lookup"><span data-stu-id="8ceb8-134">-Group</span></span>
<span data-ttu-id="8ceb8-135">Ange ACL-post för katalog för gruppen.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="8ceb8-136">-GroupOwner</span></span>
<span data-ttu-id="8ceb8-137">Ange ACL-post för katalog för grupp ägare.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="8ceb8-138">-ItemType</span></span>
<span data-ttu-id="8ceb8-139">Anger typen av katalog eller katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="8ceb8-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8ceb8-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ceb8-141">Katalogisering</span><span class="sxs-lookup"><span data-stu-id="8ceb8-141">Catalog</span></span>
- <span data-ttu-id="8ceb8-142">Databas</span><span class="sxs-lookup"><span data-stu-id="8ceb8-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8ceb8-143">-ObjectId</span></span>
<span data-ttu-id="8ceb8-144">Identiteten för användaren som ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-145">-Annat</span><span class="sxs-lookup"><span data-stu-id="8ceb8-145">-Other</span></span>
<span data-ttu-id="8ceb8-146">Ange ACL-post för andra kataloger.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-147">-Path</span><span class="sxs-lookup"><span data-stu-id="8ceb8-147">-Path</span></span>
<span data-ttu-id="8ceb8-148">Anger sökvägen till data Lake Analytics för en katalog eller katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="8ceb8-149">Delar av sökvägen ska avgränsas med en punkt (.).</span><span class="sxs-lookup"><span data-stu-id="8ceb8-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-150">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="8ceb8-150">-Permissions</span></span>
<span data-ttu-id="8ceb8-151">Anger behörigheten för åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="8ceb8-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8ceb8-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ceb8-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="8ceb8-153">None</span></span>
- <span data-ttu-id="8ceb8-154">Läst</span><span class="sxs-lookup"><span data-stu-id="8ceb8-154">Read</span></span>
- <span data-ttu-id="8ceb8-155">Läs</span><span class="sxs-lookup"><span data-stu-id="8ceb8-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-156">-Användare</span><span class="sxs-lookup"><span data-stu-id="8ceb8-156">-User</span></span>
<span data-ttu-id="8ceb8-157">Ange ACL-post för katalog för användare.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="8ceb8-158">-UserOwner</span></span>
<span data-ttu-id="8ceb8-159">Ange ACL-post för katalog för användarens ägare.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ceb8-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ceb8-160">-Confirm</span></span>
<span data-ttu-id="8ceb8-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ceb8-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ceb8-162">-WhatIf</span></span>
<span data-ttu-id="8ceb8-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ceb8-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ceb8-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ceb8-165">CommonParameters</span></span>
<span data-ttu-id="8ceb8-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ceb8-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ceb8-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ceb8-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ceb8-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ceb8-168">INPUTS</span></span>

### <span data-ttu-id="8ceb8-169">System. String</span><span class="sxs-lookup"><span data-stu-id="8ceb8-169">System.String</span></span>

### <span data-ttu-id="8ceb8-170">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8ceb8-170">System.Guid</span></span>

### <span data-ttu-id="8ceb8-171">Microsoft. Azure. commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="8ceb8-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="8ceb8-172">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + PermissionType</span><span class="sxs-lookup"><span data-stu-id="8ceb8-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="8ceb8-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ceb8-173">OUTPUTS</span></span>

### <span data-ttu-id="8ceb8-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="8ceb8-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="8ceb8-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ceb8-175">NOTES</span></span>

## <span data-ttu-id="8ceb8-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ceb8-176">RELATED LINKS</span></span>

[<span data-ttu-id="8ceb8-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8ceb8-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="8ceb8-178">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8ceb8-178">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="8ceb8-179">U-SQL erbjuder nu åtkomst kontroll på databas nivå</span><span class="sxs-lookup"><span data-stu-id="8ceb8-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
