---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 426fc5c6cac67da7b0380b3a5e5e40cc1b533366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756302"
---
# <span data-ttu-id="bddc6-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="bddc6-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="bddc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bddc6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bddc6-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bddc6-103">SYNTAX</span></span>

### <span data-ttu-id="bddc6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="bddc6-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bddc6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="bddc6-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bddc6-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bddc6-106">DESCRIPTION</span></span>
<span data-ttu-id="bddc6-107">Cmdleten **Get-AzureRmWebAppBackupConfiguration** hämtar säkerhets kopierings konfigurationen för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bddc6-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="bddc6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bddc6-108">EXAMPLES</span></span>

### <span data-ttu-id="bddc6-109">9.1</span><span class="sxs-lookup"><span data-stu-id="bddc6-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="bddc6-110">Med det här kommandot får du säkerhets kopian från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="bddc6-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="bddc6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bddc6-111">PARAMETERS</span></span>

### <span data-ttu-id="bddc6-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="bddc6-112">-Name</span></span>
<span data-ttu-id="bddc6-113">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="bddc6-113">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bddc6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bddc6-114">-ResourceGroupName</span></span>
<span data-ttu-id="bddc6-115">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bddc6-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bddc6-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="bddc6-116">-Slot</span></span>
<span data-ttu-id="bddc6-117">Plats namn</span><span class="sxs-lookup"><span data-stu-id="bddc6-117">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bddc6-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bddc6-118">-WebApp</span></span>
<span data-ttu-id="bddc6-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="bddc6-119">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bddc6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bddc6-120">-DefaultProfile</span></span>
<span data-ttu-id="bddc6-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bddc6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bddc6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bddc6-122">CommonParameters</span></span>
<span data-ttu-id="bddc6-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bddc6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bddc6-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bddc6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bddc6-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bddc6-125">INPUTS</span></span>

### <span data-ttu-id="bddc6-126">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="bddc6-126">Site</span></span>
<span data-ttu-id="bddc6-127">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bddc6-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bddc6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bddc6-128">OUTPUTS</span></span>

### <span data-ttu-id="bddc6-129">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="bddc6-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="bddc6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bddc6-130">NOTES</span></span>

## <span data-ttu-id="bddc6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bddc6-131">RELATED LINKS</span></span>

