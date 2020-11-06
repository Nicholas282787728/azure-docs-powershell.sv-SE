---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582695"
---
# <span data-ttu-id="a0f67-101">New-AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="a0f67-101">New-AzureRmDataMigrationFileShare</span></span>

## <span data-ttu-id="a0f67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0f67-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f67-103">Skapar FileShare-objektet för Azure Database migration-tjänsten, som anger den lokala nätverks resursen som käll databasens säkerhets kopior ska skapas för.</span><span class="sxs-lookup"><span data-stu-id="a0f67-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0f67-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0f67-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0f67-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f67-106">New-AzureRmDataMigrationFileShare-cmdleten skapar ett FileShare-objekt som anger den lokala nätverks delning som Azure Database migration-tjänsten kan använda för att säkerhetskopiera käll databasen.</span><span class="sxs-lookup"><span data-stu-id="a0f67-106">The New-AzureRmDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="a0f67-107">Tjänst kontot med SQL Server-instansen för källa måste ha skrivrättigheter för den här nätverks resursen.</span><span class="sxs-lookup"><span data-stu-id="a0f67-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="a0f67-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0f67-108">EXAMPLES</span></span>

### <span data-ttu-id="a0f67-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a0f67-109">Example 1</span></span>
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="a0f67-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0f67-110">PARAMETERS</span></span>

### <span data-ttu-id="a0f67-111">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="a0f67-111">-Credential</span></span>
<span data-ttu-id="a0f67-112">Autentiseringsuppgifter för åtkomst till fil resursen.</span><span class="sxs-lookup"><span data-stu-id="a0f67-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f67-113">-DefaultProfile</span></span>
<span data-ttu-id="a0f67-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f67-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a0f67-115">-Path</span></span>
<span data-ttu-id="a0f67-116">Sökväg till fil resurs.</span><span class="sxs-lookup"><span data-stu-id="a0f67-116">File share path.</span></span>

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

### <span data-ttu-id="a0f67-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f67-117">CommonParameters</span></span>
<span data-ttu-id="a0f67-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f67-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f67-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f67-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f67-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0f67-120">INPUTS</span></span>

### <span data-ttu-id="a0f67-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="a0f67-121">None</span></span>

## <span data-ttu-id="a0f67-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0f67-122">OUTPUTS</span></span>

### <span data-ttu-id="a0f67-123">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="a0f67-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="a0f67-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0f67-124">NOTES</span></span>

## <span data-ttu-id="a0f67-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0f67-125">RELATED LINKS</span></span>
