---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
ms.openlocfilehash: f44b6f370b1431a5baf1a0686b4e893653327227
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931105"
---
# <span data-ttu-id="3e4f3-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="3e4f3-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="3e4f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e4f3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e4f3-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e4f3-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e4f3-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e4f3-104">DESCRIPTION</span></span>
<span data-ttu-id="3e4f3-105">Cmdleten **New-AzureRmWebAppDatabaseBackupSetting** skapar en ny Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="3e4f3-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e4f3-106">EXAMPLES</span></span>

### <span data-ttu-id="3e4f3-107">9.1</span><span class="sxs-lookup"><span data-stu-id="3e4f3-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="3e4f3-108">Skapar en säkerhets kopierings inställning för databasen (anslutnings sträng) av typen SqlAzure för den angivna app-ContosoWebApp i resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3e4f3-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e4f3-109">PARAMETERS</span></span>

### <span data-ttu-id="3e4f3-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3e4f3-110">-ConnectionString</span></span>
<span data-ttu-id="3e4f3-111">Anslutnings sträng</span><span class="sxs-lookup"><span data-stu-id="3e4f3-111">Connection String</span></span>

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

### <span data-ttu-id="3e4f3-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="3e4f3-112">-ConnectionStringName</span></span>
<span data-ttu-id="3e4f3-113">Namn på anslutnings strängen</span><span class="sxs-lookup"><span data-stu-id="3e4f3-113">Connection String Name</span></span>

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

### <span data-ttu-id="3e4f3-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="3e4f3-114">-DatabaseType</span></span>
<span data-ttu-id="3e4f3-115">Databas typ (till exempel "SqlAzure" eller "MySql")</span><span class="sxs-lookup"><span data-stu-id="3e4f3-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="3e4f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4f3-116">-DefaultProfile</span></span>
<span data-ttu-id="3e4f3-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e4f3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e4f3-118">-Name</span></span>
<span data-ttu-id="3e4f3-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="3e4f3-119">WebApp Name</span></span>

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

### <span data-ttu-id="3e4f3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4f3-120">CommonParameters</span></span>
<span data-ttu-id="3e4f3-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4f3-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e4f3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4f3-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e4f3-123">INPUTS</span></span>

### <span data-ttu-id="3e4f3-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="3e4f3-124">None</span></span>
<span data-ttu-id="3e4f3-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e4f3-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e4f3-126">OUTPUTS</span></span>

### <span data-ttu-id="3e4f3-127">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="3e4f3-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="3e4f3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e4f3-128">NOTES</span></span>

## <span data-ttu-id="3e4f3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e4f3-129">RELATED LINKS</span></span>

