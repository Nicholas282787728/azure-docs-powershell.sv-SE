---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 4187addb4a256e3304ea5fc8a7bdfb19ed71ac46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916949"
---
# <span data-ttu-id="7b490-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7b490-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="7b490-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b490-102">SYNOPSIS</span></span>
<span data-ttu-id="7b490-103">Ändrar en post i ACL för en katalog eller katalog objekt i data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7b490-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="7b490-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b490-104">SYNTAX</span></span>

### <span data-ttu-id="7b490-105">SetCatalogAclEntryForUser (standard)</span><span class="sxs-lookup"><span data-stu-id="7b490-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b490-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="7b490-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b490-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="7b490-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b490-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="7b490-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b490-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="7b490-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b490-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="7b490-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b490-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="7b490-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b490-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="7b490-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b490-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="7b490-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b490-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="7b490-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b490-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b490-115">DESCRIPTION</span></span>
<span data-ttu-id="7b490-116">Cmdleten **set-AzDataLakeAnalyticsCatalogItemAclEntry** lägger till eller ändrar en post (ACE) i åtkomst kontrol listan (ACL) för en katalog eller katalog objekt i data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7b490-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="7b490-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b490-117">EXAMPLES</span></span>

### <span data-ttu-id="7b490-118">Exempel 1: ändra användar behörigheter för en katalog</span><span class="sxs-lookup"><span data-stu-id="7b490-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="7b490-119">Det här kommandot ändrar katalogens ACE för Patti Nilsson till Läs behörighet.</span><span class="sxs-lookup"><span data-stu-id="7b490-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="7b490-120">Exempel 2: ändra användar behörigheter för en databas</span><span class="sxs-lookup"><span data-stu-id="7b490-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="7b490-121">Det här kommandot ändrar databasens ACE för Patti Nilsson till Läs behörighet.</span><span class="sxs-lookup"><span data-stu-id="7b490-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="7b490-122">Exempel 3: ändra andra behörigheter för en katalog</span><span class="sxs-lookup"><span data-stu-id="7b490-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="7b490-123">Det här kommandot ändrar katalogens ACE för att få Läs behörighet.</span><span class="sxs-lookup"><span data-stu-id="7b490-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="7b490-124">Exempel 4: ändra andra behörigheter för en databas</span><span class="sxs-lookup"><span data-stu-id="7b490-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="7b490-125">Exempel 5: ändra behörigheter för användar ägare för en katalog</span><span class="sxs-lookup"><span data-stu-id="7b490-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="7b490-126">Det här kommandot anger ägar behörigheten för kontot som ska läsas.</span><span class="sxs-lookup"><span data-stu-id="7b490-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="7b490-127">Exempel 6: ändra behörigheter för användar ägare för en databas</span><span class="sxs-lookup"><span data-stu-id="7b490-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="7b490-128">Det här kommandot anger ägar behörighet för databasen att läsa.</span><span class="sxs-lookup"><span data-stu-id="7b490-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="7b490-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b490-129">PARAMETERS</span></span>

### <span data-ttu-id="7b490-130">-Konto</span><span class="sxs-lookup"><span data-stu-id="7b490-130">-Account</span></span>
<span data-ttu-id="7b490-131">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="7b490-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7b490-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b490-132">-DefaultProfile</span></span>
<span data-ttu-id="7b490-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b490-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b490-134">-Grupp</span><span class="sxs-lookup"><span data-stu-id="7b490-134">-Group</span></span>
<span data-ttu-id="7b490-135">Ange ACL-post för katalog för gruppen.</span><span class="sxs-lookup"><span data-stu-id="7b490-135">Set ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="7b490-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="7b490-136">-GroupOwner</span></span>
<span data-ttu-id="7b490-137">Ange ACL-post för katalog för grupp ägare.</span><span class="sxs-lookup"><span data-stu-id="7b490-137">Set ACL entry of catalog for group owner.</span></span>

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

### <span data-ttu-id="7b490-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="7b490-138">-ItemType</span></span>
<span data-ttu-id="7b490-139">Anger typen av katalog eller katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="7b490-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="7b490-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7b490-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7b490-141">Katalogisering</span><span class="sxs-lookup"><span data-stu-id="7b490-141">Catalog</span></span>
- <span data-ttu-id="7b490-142">Databas</span><span class="sxs-lookup"><span data-stu-id="7b490-142">Database</span></span>

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

### <span data-ttu-id="7b490-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7b490-143">-ObjectId</span></span>
<span data-ttu-id="7b490-144">Identiteten för användaren som ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="7b490-144">The identity of the user to set.</span></span>

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

### <span data-ttu-id="7b490-145">-Annat</span><span class="sxs-lookup"><span data-stu-id="7b490-145">-Other</span></span>
<span data-ttu-id="7b490-146">Ange ACL-post för andra kataloger.</span><span class="sxs-lookup"><span data-stu-id="7b490-146">Set ACL entry of catalog for other.</span></span>

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

### <span data-ttu-id="7b490-147">-Path</span><span class="sxs-lookup"><span data-stu-id="7b490-147">-Path</span></span>
<span data-ttu-id="7b490-148">Anger sökvägen till data Lake Analytics för en katalog eller katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="7b490-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="7b490-149">Delar av sökvägen ska avgränsas med en punkt (.).</span><span class="sxs-lookup"><span data-stu-id="7b490-149">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="7b490-150">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="7b490-150">-Permissions</span></span>
<span data-ttu-id="7b490-151">Anger behörigheten för åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="7b490-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="7b490-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7b490-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7b490-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="7b490-153">None</span></span>
- <span data-ttu-id="7b490-154">Läst</span><span class="sxs-lookup"><span data-stu-id="7b490-154">Read</span></span>
- <span data-ttu-id="7b490-155">Läs</span><span class="sxs-lookup"><span data-stu-id="7b490-155">ReadWrite</span></span>

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

### <span data-ttu-id="7b490-156">-Användare</span><span class="sxs-lookup"><span data-stu-id="7b490-156">-User</span></span>
<span data-ttu-id="7b490-157">Ange ACL-post för katalog för användare.</span><span class="sxs-lookup"><span data-stu-id="7b490-157">Set ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="7b490-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="7b490-158">-UserOwner</span></span>
<span data-ttu-id="7b490-159">Ange ACL-post för katalog för användarens ägare.</span><span class="sxs-lookup"><span data-stu-id="7b490-159">Set ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="7b490-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b490-160">-Confirm</span></span>
<span data-ttu-id="7b490-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b490-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b490-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b490-162">-WhatIf</span></span>
<span data-ttu-id="7b490-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b490-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b490-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b490-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b490-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b490-165">CommonParameters</span></span>
<span data-ttu-id="7b490-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b490-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b490-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b490-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b490-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b490-168">INPUTS</span></span>

### <span data-ttu-id="7b490-169">System. String</span><span class="sxs-lookup"><span data-stu-id="7b490-169">System.String</span></span>

### <span data-ttu-id="7b490-170">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7b490-170">System.Guid</span></span>

### <span data-ttu-id="7b490-171">Microsoft. Azure. commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="7b490-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="7b490-172">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + PermissionType</span><span class="sxs-lookup"><span data-stu-id="7b490-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="7b490-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b490-173">OUTPUTS</span></span>

### <span data-ttu-id="7b490-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="7b490-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="7b490-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b490-175">NOTES</span></span>

## <span data-ttu-id="7b490-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b490-176">RELATED LINKS</span></span>

[<span data-ttu-id="7b490-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7b490-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="7b490-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7b490-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="7b490-179">U-SQL erbjuder nu åtkomst kontroll på databas nivå</span><span class="sxs-lookup"><span data-stu-id="7b490-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)