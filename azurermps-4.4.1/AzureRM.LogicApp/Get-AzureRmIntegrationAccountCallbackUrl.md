---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 6cbb37eb211c766959f2513abe3bbe1554bfdb23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574637"
---
# <span data-ttu-id="10340-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="10340-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="10340-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10340-102">SYNOPSIS</span></span>
<span data-ttu-id="10340-103">Hämtar en URL för en återuppringnings konto.</span><span class="sxs-lookup"><span data-stu-id="10340-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10340-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10340-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10340-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10340-105">DESCRIPTION</span></span>
<span data-ttu-id="10340-106">Cmdleten **Get-AzureRmIntegrationAccountCallbackUrl** hämtar en URL för återuppringning från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10340-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="10340-107">Denna cmdlet returnerar ett **CallbackUrl** -objekt som representerar URL: en för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="10340-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="10340-108">Ange namnet på integrations kontot och resurs grupp namnet.</span><span class="sxs-lookup"><span data-stu-id="10340-108">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="10340-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="10340-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="10340-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="10340-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="10340-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="10340-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="10340-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="10340-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="10340-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10340-113">EXAMPLES</span></span>

### <span data-ttu-id="10340-114">Exempel 1: Hämta en URL för ett integrerings konto</span><span class="sxs-lookup"><span data-stu-id="10340-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="10340-115">Det här kommandot får en URL för återuppringning med integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="10340-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="10340-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10340-116">PARAMETERS</span></span>

### <span data-ttu-id="10340-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="10340-117">-Name</span></span>
<span data-ttu-id="10340-118">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="10340-118">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10340-119">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="10340-119">-NotAfter</span></span>
<span data-ttu-id="10340-120">Anger utgångs datumet för URL: en för återuppringning.</span><span class="sxs-lookup"><span data-stu-id="10340-120">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10340-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10340-121">-ResourceGroupName</span></span>
<span data-ttu-id="10340-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10340-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10340-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10340-123">-DefaultProfile</span></span>
<span data-ttu-id="10340-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10340-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10340-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10340-125">CommonParameters</span></span>
<span data-ttu-id="10340-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10340-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10340-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10340-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10340-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10340-128">INPUTS</span></span>

## <span data-ttu-id="10340-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10340-129">OUTPUTS</span></span>

### <span data-ttu-id="10340-130">Microsoft. Azure. Management. Logic. Models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="10340-130">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="10340-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10340-131">NOTES</span></span>

## <span data-ttu-id="10340-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10340-132">RELATED LINKS</span></span>

[<span data-ttu-id="10340-133">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="10340-133">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)


