---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392448"
---
# <span data-ttu-id="6749b-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="6749b-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="6749b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6749b-102">SYNOPSIS</span></span>
<span data-ttu-id="6749b-103">Hämta listan med webb program plats konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="6749b-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="6749b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6749b-104">SYNTAX</span></span>

### <span data-ttu-id="6749b-105">S</span><span class="sxs-lookup"><span data-stu-id="6749b-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6749b-106">S2</span><span class="sxs-lookup"><span data-stu-id="6749b-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6749b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6749b-107">DESCRIPTION</span></span>
<span data-ttu-id="6749b-108">Cmdleten **Get-AzWebAppSlotConfigName** hämtar listan över program inställningar och anslutnings Strängs namn som för närvarande är markerade som plats inställningar</span><span class="sxs-lookup"><span data-stu-id="6749b-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="6749b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6749b-109">EXAMPLES</span></span>

### <span data-ttu-id="6749b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6749b-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="6749b-111">Det här kommandot får program inställningar och anslutnings strängar som hör till webb programmet som heter ContosoSite associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="6749b-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="6749b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6749b-112">PARAMETERS</span></span>

### <span data-ttu-id="6749b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6749b-113">-DefaultProfile</span></span>
<span data-ttu-id="6749b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6749b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6749b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6749b-115">-Name</span></span>
<span data-ttu-id="6749b-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="6749b-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6749b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6749b-117">-ResourceGroupName</span></span>
<span data-ttu-id="6749b-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6749b-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6749b-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6749b-119">-WebApp</span></span>
<span data-ttu-id="6749b-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="6749b-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6749b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6749b-121">CommonParameters</span></span>
<span data-ttu-id="6749b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6749b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6749b-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6749b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6749b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6749b-124">INPUTS</span></span>

### <span data-ttu-id="6749b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6749b-125">System.String</span></span>

### <span data-ttu-id="6749b-126">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="6749b-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6749b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6749b-127">OUTPUTS</span></span>

### <span data-ttu-id="6749b-128">Microsoft. Azure. Management. webbplatser. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="6749b-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="6749b-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6749b-129">NOTES</span></span>

## <span data-ttu-id="6749b-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6749b-130">RELATED LINKS</span></span>
