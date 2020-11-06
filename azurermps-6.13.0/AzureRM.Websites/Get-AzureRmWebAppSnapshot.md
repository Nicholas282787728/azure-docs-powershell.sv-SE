---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572555"
---
# <span data-ttu-id="433d8-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="433d8-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="433d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="433d8-102">SYNOPSIS</span></span>
<span data-ttu-id="433d8-103">Hämtar ögonblicks bilderna för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="433d8-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="433d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="433d8-104">SYNTAX</span></span>

### <span data-ttu-id="433d8-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="433d8-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="433d8-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="433d8-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="433d8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="433d8-107">DESCRIPTION</span></span>
<span data-ttu-id="433d8-108">Cmdleten **Get-AzureRmWebAppSnapshot** returnerar alla stillbilder för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="433d8-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="433d8-109">Ögonblicks bilder är automatiska säkerhets kopior av filer och inställningar för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="433d8-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="433d8-110">En ögonblicks bild kan återställas med cmdleten **restore-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="433d8-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="433d8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="433d8-111">EXAMPLES</span></span>

### <span data-ttu-id="433d8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="433d8-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="433d8-113">Hämta stillbilder för ett webb program med namnet "ConstosoApp" med en plats med namnet "mellanlagring" i resurs gruppen "default-Web-West"</span><span class="sxs-lookup"><span data-stu-id="433d8-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="433d8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="433d8-114">PARAMETERS</span></span>

### <span data-ttu-id="433d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433d8-115">-DefaultProfile</span></span>
<span data-ttu-id="433d8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="433d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433d8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="433d8-117">-Name</span></span>
<span data-ttu-id="433d8-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="433d8-118">The name of the web app.</span></span>

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

### <span data-ttu-id="433d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="433d8-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="433d8-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="433d8-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="433d8-121">-Slot</span></span>
<span data-ttu-id="433d8-122">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="433d8-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="433d8-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="433d8-123">-WebApp</span></span>
<span data-ttu-id="433d8-124">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="433d8-124">The web app object</span></span>

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

### <span data-ttu-id="433d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433d8-125">CommonParameters</span></span>
<span data-ttu-id="433d8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433d8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="433d8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433d8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="433d8-128">INPUTS</span></span>

### <span data-ttu-id="433d8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="433d8-129">System.String</span></span>

### <span data-ttu-id="433d8-130">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="433d8-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="433d8-131">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="433d8-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="433d8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="433d8-132">OUTPUTS</span></span>

### <span data-ttu-id="433d8-133">Microsoft. Azure. kommandon. webapps. cmdletar. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="433d8-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="433d8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="433d8-134">NOTES</span></span>

## <span data-ttu-id="433d8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="433d8-135">RELATED LINKS</span></span>
