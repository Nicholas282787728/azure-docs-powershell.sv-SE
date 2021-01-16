---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409192"
---
# <span data-ttu-id="14110-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="14110-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="14110-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14110-102">SYNOPSIS</span></span>
<span data-ttu-id="14110-103">Hämtar en URL för en återuppringnings konto.</span><span class="sxs-lookup"><span data-stu-id="14110-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="14110-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14110-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14110-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14110-105">DESCRIPTION</span></span>
<span data-ttu-id="14110-106">Cmdleten **Get-AzIntegrationAccountCallbackUrl** hämtar en URL för återuppringning från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="14110-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="14110-107">Denna cmdlet returnerar ett **CallbackUrl** -objekt som representerar URL: en för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="14110-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="14110-108">Ange namnet på integrations kontot och resurs grupp namnet.</span><span class="sxs-lookup"><span data-stu-id="14110-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="14110-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="14110-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="14110-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="14110-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="14110-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="14110-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="14110-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="14110-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="14110-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14110-113">EXAMPLES</span></span>

### <span data-ttu-id="14110-114">Exempel 1: Hämta en URL för ett integrerings konto</span><span class="sxs-lookup"><span data-stu-id="14110-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="14110-115">Det här kommandot får en URL för återuppringning med integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="14110-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="14110-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14110-116">PARAMETERS</span></span>

### <span data-ttu-id="14110-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14110-117">-DefaultProfile</span></span>
<span data-ttu-id="14110-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="14110-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14110-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="14110-119">-Name</span></span>
<span data-ttu-id="14110-120">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="14110-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="14110-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="14110-121">-NotAfter</span></span>
<span data-ttu-id="14110-122">Anger utgångs datumet för URL: en för återuppringning.</span><span class="sxs-lookup"><span data-stu-id="14110-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="14110-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14110-123">-ResourceGroupName</span></span>
<span data-ttu-id="14110-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="14110-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="14110-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14110-125">CommonParameters</span></span>
<span data-ttu-id="14110-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14110-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14110-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14110-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14110-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14110-128">INPUTS</span></span>

### <span data-ttu-id="14110-129">System. String</span><span class="sxs-lookup"><span data-stu-id="14110-129">System.String</span></span>

## <span data-ttu-id="14110-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14110-130">OUTPUTS</span></span>

### <span data-ttu-id="14110-131">Microsoft. Azure. Management. Logic. Models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="14110-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="14110-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14110-132">NOTES</span></span>

## <span data-ttu-id="14110-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14110-133">RELATED LINKS</span></span>

[<span data-ttu-id="14110-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="14110-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


