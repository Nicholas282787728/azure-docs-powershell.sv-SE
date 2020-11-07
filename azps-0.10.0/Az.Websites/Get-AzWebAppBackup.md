---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: b533d63e83d731dd5b95788609d32fa4cf7863f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923374"
---
# <span data-ttu-id="a5141-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a5141-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="a5141-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5141-102">SYNOPSIS</span></span>

## <span data-ttu-id="a5141-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5141-103">SYNTAX</span></span>

### <span data-ttu-id="a5141-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a5141-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5141-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a5141-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5141-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5141-106">DESCRIPTION</span></span>
<span data-ttu-id="a5141-107">Cmdleten **Get-AzWebAppBackup** hämtar den angivna säkerhets kopian av ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a5141-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="a5141-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5141-108">EXAMPLES</span></span>

### <span data-ttu-id="a5141-109">9.1</span><span class="sxs-lookup"><span data-stu-id="a5141-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="a5141-110">Med det här kommandot får du säkerhets kopian med ID: t "12345" från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="a5141-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a5141-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5141-111">PARAMETERS</span></span>

### <span data-ttu-id="a5141-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="a5141-112">-BackupId</span></span>
<span data-ttu-id="a5141-113">Säkerhets kopie-ID</span><span class="sxs-lookup"><span data-stu-id="a5141-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5141-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5141-114">-DefaultProfile</span></span>
<span data-ttu-id="a5141-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5141-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5141-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5141-116">-Name</span></span>
<span data-ttu-id="a5141-117">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="a5141-117">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5141-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5141-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5141-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a5141-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5141-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="a5141-120">-Slot</span></span>
<span data-ttu-id="a5141-121">Plats namn</span><span class="sxs-lookup"><span data-stu-id="a5141-121">Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5141-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a5141-122">-WebApp</span></span>
<span data-ttu-id="a5141-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="a5141-123">Piped WebApp</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5141-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5141-124">CommonParameters</span></span>
<span data-ttu-id="a5141-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5141-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5141-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5141-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5141-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5141-127">INPUTS</span></span>

### <span data-ttu-id="a5141-128">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="a5141-128">Site</span></span>
<span data-ttu-id="a5141-129">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a5141-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a5141-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5141-130">OUTPUTS</span></span>

### <span data-ttu-id="a5141-131">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a5141-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="a5141-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5141-132">NOTES</span></span>

## <span data-ttu-id="a5141-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5141-133">RELATED LINKS</span></span>

