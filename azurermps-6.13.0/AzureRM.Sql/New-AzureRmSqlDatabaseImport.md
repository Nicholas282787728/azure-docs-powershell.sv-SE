---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 4ea8a6aca74634e8105026e45c25b861e8c060f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576733"
---
# <span data-ttu-id="b1c49-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b1c49-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="b1c49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1c49-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c49-103">Importera en. bacpac-fil och skapa en ny databas på servern.</span><span class="sxs-lookup"><span data-stu-id="b1c49-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1c49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1c49-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1c49-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1c49-105">DESCRIPTION</span></span>
<span data-ttu-id="b1c49-106">Cmdleten **New-AzureRmSqlDatabaseImport** importerar en BACPAC-fil från ett Azure Storage-konto till en ny Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="b1c49-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="b1c49-107">Status förfrågan för hämta import databas kan skickas för att hämta statusinformation för denna begäran.</span><span class="sxs-lookup"><span data-stu-id="b1c49-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="b1c49-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1c49-108">EXAMPLES</span></span>

### <span data-ttu-id="b1c49-109">Exempel 1: skapa en import förfrågan för en BACPAC-fil</span><span class="sxs-lookup"><span data-stu-id="b1c49-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="b1c49-110">Det här kommandot skapar en import förfrågan för att importera en. BACPAC till en ny databas.</span><span class="sxs-lookup"><span data-stu-id="b1c49-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="b1c49-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1c49-111">PARAMETERS</span></span>

### <span data-ttu-id="b1c49-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="b1c49-112">-AdministratorLogin</span></span>
<span data-ttu-id="b1c49-113">Anger namnet på SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="b1c49-113">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b1c49-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b1c49-115">Anger lösen ordet för SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="b1c49-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b1c49-116">-AuthenticationType</span></span>
<span data-ttu-id="b1c49-117">Anger vilken typ av verifikation som används för att komma åt servern.</span><span class="sxs-lookup"><span data-stu-id="b1c49-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="b1c49-118">Den här parametern använder SQL om ingen autentiseringstyp är angiven.</span><span class="sxs-lookup"><span data-stu-id="b1c49-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="b1c49-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b1c49-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1c49-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="b1c49-120">SQL.</span></span>
<span data-ttu-id="b1c49-121">SQL-verifikation.</span><span class="sxs-lookup"><span data-stu-id="b1c49-121">SQL authentication.</span></span>
<span data-ttu-id="b1c49-122">Ange *AdministratorLogin* -och *AdministratorLoginPassword* -parametrarna till SQL-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="b1c49-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="b1c49-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="b1c49-123">ADPassword.</span></span>
<span data-ttu-id="b1c49-124">Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="b1c49-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="b1c49-125">Ange *AdministratorLogin* och *AdministratorLoginPassword* till Azure Active Directory-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="b1c49-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="b1c49-126">Den här parametern är endast tillgänglig på V12-servrar för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="b1c49-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="b1c49-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="b1c49-128">Anger den maximala storleken för den nyligen importerade databasen.</span><span class="sxs-lookup"><span data-stu-id="b1c49-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1c49-129">-DatabaseName</span></span>
<span data-ttu-id="b1c49-130">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b1c49-130">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c49-131">-DefaultProfile</span></span>
<span data-ttu-id="b1c49-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b1c49-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1c49-133">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="b1c49-133">-Edition</span></span>
<span data-ttu-id="b1c49-134">Anger den version av den nya databasen som du vill importera till.</span><span class="sxs-lookup"><span data-stu-id="b1c49-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="b1c49-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b1c49-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1c49-136">Beta</span><span class="sxs-lookup"><span data-stu-id="b1c49-136">Premium</span></span>
- <span data-ttu-id="b1c49-137">Basisk</span><span class="sxs-lookup"><span data-stu-id="b1c49-137">Basic</span></span>
- <span data-ttu-id="b1c49-138">Standar</span><span class="sxs-lookup"><span data-stu-id="b1c49-138">Standard</span></span>
- <span data-ttu-id="b1c49-139">Warehouse</span><span class="sxs-lookup"><span data-stu-id="b1c49-139">DataWarehouse</span></span>
- <span data-ttu-id="b1c49-140">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="b1c49-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c49-141">-ResourceGroupName</span></span>
<span data-ttu-id="b1c49-142">Anger namnet på resurs gruppen för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="b1c49-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="b1c49-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b1c49-143">-ServerName</span></span>
<span data-ttu-id="b1c49-144">Anger namnet på SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="b1c49-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="b1c49-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b1c49-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="b1c49-146">Anger namnet på det tjänst mål som ska kopplas till Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b1c49-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="b1c49-147">-StorageKey</span></span>
<span data-ttu-id="b1c49-148">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b1c49-148">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="b1c49-149">-StorageKeyType</span></span>
<span data-ttu-id="b1c49-150">Anger typen av åtkomst nycklar för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b1c49-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="b1c49-151">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b1c49-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1c49-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="b1c49-152">StorageAccessKey.</span></span>
<span data-ttu-id="b1c49-153">Använder lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b1c49-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="b1c49-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="b1c49-154">SharedAccessKey.</span></span>
<span data-ttu-id="b1c49-155">Använder den delade Access-signaturen (SAS).</span><span class="sxs-lookup"><span data-stu-id="b1c49-155">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="b1c49-156">-StorageUri</span></span>
<span data-ttu-id="b1c49-157">Anger BLOB URI för. bacpac-filen.</span><span class="sxs-lookup"><span data-stu-id="b1c49-157">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b1c49-158">-Confirm</span></span>
<span data-ttu-id="b1c49-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1c49-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c49-160">-WhatIf</span></span>
<span data-ttu-id="b1c49-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b1c49-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c49-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b1c49-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c49-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c49-163">CommonParameters</span></span>
<span data-ttu-id="b1c49-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c49-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c49-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c49-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c49-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1c49-166">INPUTS</span></span>

### <span data-ttu-id="b1c49-167">System. String</span><span class="sxs-lookup"><span data-stu-id="b1c49-167">System.String</span></span>

## <span data-ttu-id="b1c49-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1c49-168">OUTPUTS</span></span>

### <span data-ttu-id="b1c49-169">Microsoft. Azure. commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="b1c49-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="b1c49-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1c49-170">NOTES</span></span>
* <span data-ttu-id="b1c49-171">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="b1c49-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b1c49-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1c49-172">RELATED LINKS</span></span>

[<span data-ttu-id="b1c49-173">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="b1c49-173">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="b1c49-174">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b1c49-174">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="b1c49-175">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="b1c49-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

