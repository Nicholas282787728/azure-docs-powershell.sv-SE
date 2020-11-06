---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577763"
---
# <span data-ttu-id="b4516-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b4516-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="b4516-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4516-102">SYNOPSIS</span></span>
<span data-ttu-id="b4516-103">Tar bort webb program i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b4516-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4516-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4516-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4516-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4516-105">DESCRIPTION</span></span>
<span data-ttu-id="b4516-106">Cmdleten **Get-AzureRmDeletedWebApp** returnerar alla borttagna webb program i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b4516-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="b4516-107">Borttagna appar kan filtreras efter resurs grupp, namn och plats.</span><span class="sxs-lookup"><span data-stu-id="b4516-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="b4516-108">Det kan finnas fler än en borttagen app med samma namn och resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b4516-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="b4516-109">Kontrol lera DeletionTime för att skilja på borttagna appar som har samma namn.</span><span class="sxs-lookup"><span data-stu-id="b4516-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="b4516-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4516-110">EXAMPLES</span></span>

### <span data-ttu-id="b4516-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4516-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b4516-112">Det här kommandot hämtar de borttagna apparna som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="b4516-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b4516-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4516-113">PARAMETERS</span></span>

### <span data-ttu-id="b4516-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4516-114">-DefaultProfile</span></span>
<span data-ttu-id="b4516-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4516-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4516-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4516-116">-Name</span></span>
<span data-ttu-id="b4516-117">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="b4516-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4516-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4516-118">-ResourceGroupName</span></span>
<span data-ttu-id="b4516-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4516-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4516-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="b4516-120">-Slot</span></span>
<span data-ttu-id="b4516-121">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="b4516-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4516-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4516-122">CommonParameters</span></span>
<span data-ttu-id="b4516-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4516-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b4516-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4516-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4516-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4516-125">INPUTS</span></span>

### <span data-ttu-id="b4516-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="b4516-126">None</span></span>

## <span data-ttu-id="b4516-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4516-127">OUTPUTS</span></span>

### <span data-ttu-id="b4516-128">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b4516-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="b4516-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4516-129">NOTES</span></span>

## <span data-ttu-id="b4516-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4516-130">RELATED LINKS</span></span>

[<span data-ttu-id="b4516-131">Återställ-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b4516-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
