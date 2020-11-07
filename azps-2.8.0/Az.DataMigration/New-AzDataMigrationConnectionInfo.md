---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: 871b6c09832e4b857a616c93cc33102f2dd0ad8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744509"
---
# <span data-ttu-id="f5e23-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="f5e23-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="f5e23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5e23-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e23-103">Skapar en ny anslutnings information ett objekt som anger Server typ och namn för anslutning.</span><span class="sxs-lookup"><span data-stu-id="f5e23-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="f5e23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5e23-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5e23-105">DESCRIPTION</span></span>
<span data-ttu-id="f5e23-106">New-AzDataMigrationConnectionInfo cmdlet skapar ny en anslutnings information som anger Server typen för anslutning.</span><span class="sxs-lookup"><span data-stu-id="f5e23-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="f5e23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5e23-107">EXAMPLES</span></span>

### <span data-ttu-id="f5e23-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5e23-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="f5e23-109">I det föregående exemplet skapas en ny anslutnings information med parametern SQL as ServerType.</span><span class="sxs-lookup"><span data-stu-id="f5e23-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="f5e23-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5e23-110">PARAMETERS</span></span>

### <span data-ttu-id="f5e23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e23-111">-DefaultProfile</span></span>
<span data-ttu-id="f5e23-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e23-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5e23-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="f5e23-113">-ServerType</span></span>
<span data-ttu-id="f5e23-114">Fasttext som beskriver Server typen som du vill ansluta till.</span><span class="sxs-lookup"><span data-stu-id="f5e23-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="f5e23-115">Funktioner som stöds för närvarande är SQL för SQL Server, Azure SQL-hanterad instans, MongoDb, CosmosDb och Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f5e23-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e23-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e23-116">CommonParameters</span></span>
<span data-ttu-id="f5e23-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e23-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e23-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e23-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e23-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5e23-119">INPUTS</span></span>

### <span data-ttu-id="f5e23-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="f5e23-120">None</span></span>

## <span data-ttu-id="f5e23-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5e23-121">OUTPUTS</span></span>

### <span data-ttu-id="f5e23-122">Microsoft. Azure. Management. DataMigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="f5e23-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="f5e23-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5e23-123">NOTES</span></span>

## <span data-ttu-id="f5e23-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5e23-124">RELATED LINKS</span></span>
