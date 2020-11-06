---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7eea25d4b82dc8a424fea0cbd3e361014c77c396
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580903"
---
# <span data-ttu-id="6a89b-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="6a89b-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="6a89b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a89b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a89b-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a89b-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a89b-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a89b-104">DESCRIPTION</span></span>
<span data-ttu-id="6a89b-105">Cmdleten **New-AzureRmWebAppDatabaseBackupSetting** skapar en ny Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="6a89b-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="6a89b-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a89b-106">EXAMPLES</span></span>

### <span data-ttu-id="6a89b-107">9.1</span><span class="sxs-lookup"><span data-stu-id="6a89b-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="6a89b-108">Skapar en säkerhets kopierings inställning för databasen (anslutnings sträng) av typen SqlAzure för den angivna app-ContosoWebApp i resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="6a89b-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6a89b-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a89b-109">PARAMETERS</span></span>

### <span data-ttu-id="6a89b-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6a89b-110">-ConnectionString</span></span>
<span data-ttu-id="6a89b-111">Anslutnings sträng</span><span class="sxs-lookup"><span data-stu-id="6a89b-111">Connection String</span></span>

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

### <span data-ttu-id="6a89b-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="6a89b-112">-ConnectionStringName</span></span>
<span data-ttu-id="6a89b-113">Namn på anslutnings strängen</span><span class="sxs-lookup"><span data-stu-id="6a89b-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a89b-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="6a89b-114">-DatabaseType</span></span>
<span data-ttu-id="6a89b-115">Databas typ (till exempel "SqlAzure" eller "MySql")</span><span class="sxs-lookup"><span data-stu-id="6a89b-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="6a89b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a89b-116">-DefaultProfile</span></span>
<span data-ttu-id="6a89b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a89b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a89b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a89b-118">-Name</span></span>
<span data-ttu-id="6a89b-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="6a89b-119">WebApp Name</span></span>

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

### <span data-ttu-id="6a89b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a89b-120">CommonParameters</span></span>
<span data-ttu-id="6a89b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a89b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a89b-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a89b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a89b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a89b-123">INPUTS</span></span>

### <span data-ttu-id="6a89b-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="6a89b-124">None</span></span>
<span data-ttu-id="6a89b-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6a89b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a89b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a89b-126">OUTPUTS</span></span>

### <span data-ttu-id="6a89b-127">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="6a89b-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="6a89b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a89b-128">NOTES</span></span>

## <span data-ttu-id="6a89b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a89b-129">RELATED LINKS</span></span>

