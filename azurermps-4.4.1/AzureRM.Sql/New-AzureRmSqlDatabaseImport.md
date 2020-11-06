---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 8ebe1cecc42d8ee01c270b994e1e10de4f402c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576686"
---
# <span data-ttu-id="940a7-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="940a7-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="940a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="940a7-102">SYNOPSIS</span></span>
<span data-ttu-id="940a7-103">Importera en. bacpac-fil och skapa en ny databas på servern.</span><span class="sxs-lookup"><span data-stu-id="940a7-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="940a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="940a7-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="940a7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="940a7-105">DESCRIPTION</span></span>
<span data-ttu-id="940a7-106">Cmdleten **New-AzureRmSqlDatabaseImport** importerar en BACPAC-fil från ett Azure Storage-konto till en ny Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="940a7-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="940a7-107">Status förfrågan för hämta import databas kan skickas för att hämta statusinformation för denna begäran.</span><span class="sxs-lookup"><span data-stu-id="940a7-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="940a7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="940a7-108">EXAMPLES</span></span>

### <span data-ttu-id="940a7-109">Exempel 1: skapa en import förfrågan för en BACPAC-fil</span><span class="sxs-lookup"><span data-stu-id="940a7-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="940a7-110">Det här kommandot skapar en import förfrågan för att importera en. BACPAC till en ny databas.</span><span class="sxs-lookup"><span data-stu-id="940a7-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="940a7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="940a7-111">PARAMETERS</span></span>

### <span data-ttu-id="940a7-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="940a7-112">-AdministratorLogin</span></span>
<span data-ttu-id="940a7-113">Anger namnet på SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="940a7-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="940a7-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="940a7-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="940a7-115">Anger lösen ordet för SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="940a7-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="940a7-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="940a7-116">-AuthenticationType</span></span>
<span data-ttu-id="940a7-117">Anger vilken typ av verifikation som används för att komma åt servern.</span><span class="sxs-lookup"><span data-stu-id="940a7-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="940a7-118">Den här parametern använder SQL om ingen autentiseringstyp är angiven.</span><span class="sxs-lookup"><span data-stu-id="940a7-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="940a7-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="940a7-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="940a7-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="940a7-120">SQL.</span></span>
<span data-ttu-id="940a7-121">SQL-verifikation.</span><span class="sxs-lookup"><span data-stu-id="940a7-121">SQL authentication.</span></span>
<span data-ttu-id="940a7-122">Ange *AdministratorLogin* -och *AdministratorLoginPassword* -parametrarna till SQL-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="940a7-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="940a7-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="940a7-123">ADPassword.</span></span>
<span data-ttu-id="940a7-124">Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="940a7-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="940a7-125">Ange *AdministratorLogin* och *AdministratorLoginPassword* till Azure Active Directory-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="940a7-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="940a7-126">Den här parametern är endast tillgänglig på V12-servrar för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="940a7-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="940a7-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="940a7-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="940a7-128">Anger den maximala storleken för den nyligen importerade databasen.</span><span class="sxs-lookup"><span data-stu-id="940a7-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="940a7-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="940a7-129">-DatabaseName</span></span>
<span data-ttu-id="940a7-130">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="940a7-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="940a7-131">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="940a7-131">-Edition</span></span>
<span data-ttu-id="940a7-132">Anger den version av den nya databasen som du vill importera till.</span><span class="sxs-lookup"><span data-stu-id="940a7-132">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="940a7-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="940a7-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="940a7-134">Beta</span><span class="sxs-lookup"><span data-stu-id="940a7-134">Premium</span></span>
- <span data-ttu-id="940a7-135">Basisk</span><span class="sxs-lookup"><span data-stu-id="940a7-135">Basic</span></span>
- <span data-ttu-id="940a7-136">Standar</span><span class="sxs-lookup"><span data-stu-id="940a7-136">Standard</span></span>
- <span data-ttu-id="940a7-137">Warehouse</span><span class="sxs-lookup"><span data-stu-id="940a7-137">DataWarehouse</span></span>
- <span data-ttu-id="940a7-138">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="940a7-138">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940a7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940a7-139">-ResourceGroupName</span></span>
<span data-ttu-id="940a7-140">Anger namnet på resurs gruppen för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="940a7-140">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="940a7-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="940a7-141">-ServerName</span></span>
<span data-ttu-id="940a7-142">Anger namnet på SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="940a7-142">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="940a7-143">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="940a7-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="940a7-144">Anger namnet på det tjänst mål som ska kopplas till Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="940a7-144">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="940a7-145">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="940a7-145">-StorageKey</span></span>
<span data-ttu-id="940a7-146">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="940a7-146">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="940a7-147">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="940a7-147">-StorageKeyType</span></span>
<span data-ttu-id="940a7-148">Anger typen av åtkomst nycklar för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="940a7-148">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="940a7-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="940a7-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="940a7-150">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="940a7-150">StorageAccessKey.</span></span>
<span data-ttu-id="940a7-151">Använder lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="940a7-151">Uses the storage account key.</span></span> 
- <span data-ttu-id="940a7-152">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="940a7-152">SharedAccessKey.</span></span>
<span data-ttu-id="940a7-153">Använder den delade Access-signaturen (SAS).</span><span class="sxs-lookup"><span data-stu-id="940a7-153">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="940a7-154">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="940a7-154">-StorageUri</span></span>
<span data-ttu-id="940a7-155">Anger BLOB URI för. bacpac-filen.</span><span class="sxs-lookup"><span data-stu-id="940a7-155">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="940a7-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="940a7-156">-Confirm</span></span>
<span data-ttu-id="940a7-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="940a7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="940a7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="940a7-158">-WhatIf</span></span>
<span data-ttu-id="940a7-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="940a7-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="940a7-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="940a7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="940a7-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940a7-161">-DefaultProfile</span></span>
<span data-ttu-id="940a7-162">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="940a7-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="940a7-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940a7-163">CommonParameters</span></span>
<span data-ttu-id="940a7-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="940a7-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940a7-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940a7-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940a7-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="940a7-166">INPUTS</span></span>

## <span data-ttu-id="940a7-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="940a7-167">OUTPUTS</span></span>

### <span data-ttu-id="940a7-168">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="940a7-168">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="940a7-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="940a7-169">NOTES</span></span>
* <span data-ttu-id="940a7-170">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="940a7-170">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="940a7-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="940a7-171">RELATED LINKS</span></span>

[<span data-ttu-id="940a7-172">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="940a7-172">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="940a7-173">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="940a7-173">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="940a7-174">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="940a7-174">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

