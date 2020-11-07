---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4c6dc810d35feedd0d0d43e0bd3b3efb7c9b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923373"
---
# <span data-ttu-id="0b442-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b442-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="0b442-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b442-102">SYNOPSIS</span></span>

## <span data-ttu-id="0b442-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b442-103">SYNTAX</span></span>

### <span data-ttu-id="0b442-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0b442-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b442-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0b442-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b442-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b442-106">DESCRIPTION</span></span>
<span data-ttu-id="0b442-107">Cmdleten **Get-AzWebAppBackupConfiguration** hämtar säkerhets kopierings konfigurationen för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0b442-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="0b442-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b442-108">EXAMPLES</span></span>

### <span data-ttu-id="0b442-109">9.1</span><span class="sxs-lookup"><span data-stu-id="0b442-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="0b442-110">Med det här kommandot får du säkerhets kopian från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="0b442-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0b442-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b442-111">PARAMETERS</span></span>

### <span data-ttu-id="0b442-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b442-112">-DefaultProfile</span></span>
<span data-ttu-id="0b442-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b442-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b442-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="0b442-114">-Name</span></span>
<span data-ttu-id="0b442-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="0b442-115">WebApp Name</span></span>

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

### <span data-ttu-id="0b442-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b442-116">-ResourceGroupName</span></span>
<span data-ttu-id="0b442-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0b442-117">Resource Group Name</span></span>

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

### <span data-ttu-id="0b442-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="0b442-118">-Slot</span></span>
<span data-ttu-id="0b442-119">Plats namn</span><span class="sxs-lookup"><span data-stu-id="0b442-119">Slot Name</span></span>

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

### <span data-ttu-id="0b442-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0b442-120">-WebApp</span></span>
<span data-ttu-id="0b442-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="0b442-121">WebApp Name</span></span>

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

### <span data-ttu-id="0b442-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b442-122">CommonParameters</span></span>
<span data-ttu-id="0b442-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b442-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b442-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b442-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b442-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b442-125">INPUTS</span></span>

### <span data-ttu-id="0b442-126">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="0b442-126">Site</span></span>
<span data-ttu-id="0b442-127">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0b442-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0b442-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b442-128">OUTPUTS</span></span>

### <span data-ttu-id="0b442-129">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b442-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="0b442-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b442-130">NOTES</span></span>

## <span data-ttu-id="0b442-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b442-131">RELATED LINKS</span></span>

