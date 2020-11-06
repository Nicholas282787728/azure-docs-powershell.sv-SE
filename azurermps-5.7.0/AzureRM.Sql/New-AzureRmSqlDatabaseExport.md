---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 324686ace908235e3b48fb150249d2bad22c169b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573164"
---
# <span data-ttu-id="a13bc-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="a13bc-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="a13bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a13bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a13bc-103">Exporterar en Azure SQL-databas som en. bacpac-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a13bc-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a13bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a13bc-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a13bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a13bc-105">DESCRIPTION</span></span>
<span data-ttu-id="a13bc-106">Cmdleten **New-AzureRmSqlDatabaseExport** exporterar en Azure SQL-databas som en. bacpac-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a13bc-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="a13bc-107">Status förfrågan för skaffa export databas kan skickas för att hämta statusinformation för denna begäran.</span><span class="sxs-lookup"><span data-stu-id="a13bc-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="a13bc-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="a13bc-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a13bc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a13bc-109">EXAMPLES</span></span>

### <span data-ttu-id="a13bc-110">Exempel 1: skapa en export förfrågan för en databas</span><span class="sxs-lookup"><span data-stu-id="a13bc-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="a13bc-111">Det här kommandot skapar en export förfrågan för den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="a13bc-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="a13bc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a13bc-112">PARAMETERS</span></span>

### <span data-ttu-id="a13bc-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="a13bc-113">-AdministratorLogin</span></span>
<span data-ttu-id="a13bc-114">Anger namnet på SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="a13bc-114">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="a13bc-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="a13bc-116">Anger lösen ordet för SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="a13bc-116">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a13bc-117">-AuthenticationType</span></span>
<span data-ttu-id="a13bc-118">Anger vilken typ av verifikation som används för att komma åt servern.</span><span class="sxs-lookup"><span data-stu-id="a13bc-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="a13bc-119">Standardvärdet är SQL om ingen autentiseringstyp är angiven.</span><span class="sxs-lookup"><span data-stu-id="a13bc-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="a13bc-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a13bc-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a13bc-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="a13bc-121">Sql.</span></span>
<span data-ttu-id="a13bc-122">SQL-verifikation.</span><span class="sxs-lookup"><span data-stu-id="a13bc-122">SQL authentication.</span></span>
<span data-ttu-id="a13bc-123">Ställ in *AdministratorLogin* och *AdministratorLoginPassword* på SQL-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="a13bc-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="a13bc-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="a13bc-124">ADPassword.</span></span>
<span data-ttu-id="a13bc-125">Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="a13bc-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="a13bc-126">Ange *AdministratorLogin* och *ADMINISTRATORLOGINPASSWORD* till Azure AD-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="a13bc-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="a13bc-127">Den här parametern är endast tillgänglig på V12-servrar för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="a13bc-127">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a13bc-128">-DatabaseName</span></span>
<span data-ttu-id="a13bc-129">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a13bc-129">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a13bc-130">-DefaultProfile</span></span>
<span data-ttu-id="a13bc-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a13bc-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a13bc-132">-ResourceGroupName</span></span>
<span data-ttu-id="a13bc-133">Anger namnet på resurs gruppen för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="a13bc-133">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a13bc-134">-ServerName</span></span>
<span data-ttu-id="a13bc-135">Anger namnet på SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="a13bc-135">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="a13bc-136">-StorageKey</span></span>
<span data-ttu-id="a13bc-137">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a13bc-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a13bc-138">-StorageKeyType</span></span>
<span data-ttu-id="a13bc-139">Anger typen av åtkomst nycklar för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a13bc-139">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="a13bc-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a13bc-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a13bc-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="a13bc-141">StorageAccessKey.</span></span>
<span data-ttu-id="a13bc-142">I det här värdet används en lagrings konto profil.</span><span class="sxs-lookup"><span data-stu-id="a13bc-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="a13bc-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="a13bc-143">SharedAccessKey.</span></span>
<span data-ttu-id="a13bc-144">I det här värdet används en delad åtkomst-signaturnyckel (SAS).</span><span class="sxs-lookup"><span data-stu-id="a13bc-144">This value uses a Shared Access Signature (SAS) key.</span></span>

```yaml
Type: StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="a13bc-145">-StorageUri</span></span>
<span data-ttu-id="a13bc-146">Anger BLOB-länken som en URL till. bacpac-filen.</span><span class="sxs-lookup"><span data-stu-id="a13bc-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a13bc-147">-Confirm</span></span>
<span data-ttu-id="a13bc-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a13bc-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a13bc-149">-WhatIf</span></span>
<span data-ttu-id="a13bc-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a13bc-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a13bc-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a13bc-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13bc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a13bc-152">CommonParameters</span></span>
<span data-ttu-id="a13bc-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a13bc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a13bc-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a13bc-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a13bc-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a13bc-155">INPUTS</span></span>

### <span data-ttu-id="a13bc-156">Ingen</span><span class="sxs-lookup"><span data-stu-id="a13bc-156">None</span></span>
<span data-ttu-id="a13bc-157">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a13bc-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a13bc-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a13bc-158">OUTPUTS</span></span>

### <span data-ttu-id="a13bc-159">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="a13bc-159">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="a13bc-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a13bc-160">NOTES</span></span>
* <span data-ttu-id="a13bc-161">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="a13bc-161">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="a13bc-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a13bc-162">RELATED LINKS</span></span>

[<span data-ttu-id="a13bc-163">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="a13bc-163">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="a13bc-164">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="a13bc-164">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="a13bc-165">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a13bc-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
