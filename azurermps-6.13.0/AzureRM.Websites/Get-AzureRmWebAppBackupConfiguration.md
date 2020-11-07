---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 81c9d87ecd93097c7e114a312b68d25d7dd681c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755316"
---
# <span data-ttu-id="5e051-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e051-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5e051-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e051-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e051-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e051-103">SYNTAX</span></span>

### <span data-ttu-id="5e051-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5e051-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e051-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5e051-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e051-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e051-106">DESCRIPTION</span></span>
<span data-ttu-id="5e051-107">Cmdleten **Get-AzureRmWebAppBackupConfiguration** hämtar säkerhets kopierings konfigurationen för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5e051-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="5e051-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e051-108">EXAMPLES</span></span>

### <span data-ttu-id="5e051-109">9.1</span><span class="sxs-lookup"><span data-stu-id="5e051-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="5e051-110">Med det här kommandot får du säkerhets kopian från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="5e051-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5e051-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e051-111">PARAMETERS</span></span>

### <span data-ttu-id="5e051-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e051-112">-DefaultProfile</span></span>
<span data-ttu-id="5e051-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e051-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e051-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e051-114">-Name</span></span>
<span data-ttu-id="5e051-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="5e051-115">WebApp Name</span></span>

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

### <span data-ttu-id="5e051-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e051-116">-ResourceGroupName</span></span>
<span data-ttu-id="5e051-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5e051-117">Resource Group Name</span></span>

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

### <span data-ttu-id="5e051-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="5e051-118">-Slot</span></span>
<span data-ttu-id="5e051-119">Plats namn</span><span class="sxs-lookup"><span data-stu-id="5e051-119">Slot Name</span></span>

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

### <span data-ttu-id="5e051-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5e051-120">-WebApp</span></span>
<span data-ttu-id="5e051-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="5e051-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e051-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e051-122">CommonParameters</span></span>
<span data-ttu-id="5e051-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e051-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e051-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e051-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e051-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e051-125">INPUTS</span></span>

### <span data-ttu-id="5e051-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5e051-126">System.String</span></span>

### <span data-ttu-id="5e051-127">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="5e051-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="5e051-128">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e051-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="5e051-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e051-129">OUTPUTS</span></span>

### <span data-ttu-id="5e051-130">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e051-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5e051-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e051-131">NOTES</span></span>

## <span data-ttu-id="5e051-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e051-132">RELATED LINKS</span></span>
