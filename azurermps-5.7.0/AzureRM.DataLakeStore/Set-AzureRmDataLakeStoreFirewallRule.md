---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 3ad3e98e6fb2ab5c6e0b04495142861ecfe9e0ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579555"
---
# <span data-ttu-id="780c9-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="780c9-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="780c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="780c9-102">SYNOPSIS</span></span>
<span data-ttu-id="780c9-103">Ändrar den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="780c9-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="780c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="780c9-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="780c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="780c9-105">DESCRIPTION</span></span>
<span data-ttu-id="780c9-106">Cmdleten **set-AzureRmDataLakeStoreFirewallRule** ändrar den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="780c9-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="780c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="780c9-107">EXAMPLES</span></span>

### <span data-ttu-id="780c9-108">Exempel 1: Uppdatera start-och slut adress för en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="780c9-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="780c9-109">Uppdaterar brand Väggs regeln "MyFirewallRule" i kontot "ContosoADL" för att ha ett område med 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="780c9-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="780c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="780c9-110">PARAMETERS</span></span>

### <span data-ttu-id="780c9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="780c9-111">-Account</span></span>
<span data-ttu-id="780c9-112">Data Lake Store-konto för att uppdatera brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="780c9-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780c9-113">-DefaultProfile</span></span>
<span data-ttu-id="780c9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="780c9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="780c9-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="780c9-115">-EndIpAddress</span></span>
<span data-ttu-id="780c9-116">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="780c9-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="780c9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="780c9-117">-Name</span></span>
<span data-ttu-id="780c9-118">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="780c9-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="780c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="780c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="780c9-120">Anger namnet på den resurs grupp som innehåller kontot som ska uppdatera brand Väggs regeln för.</span><span class="sxs-lookup"><span data-stu-id="780c9-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="780c9-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="780c9-121">-StartIpAddress</span></span>
<span data-ttu-id="780c9-122">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="780c9-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780c9-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="780c9-123">-Confirm</span></span>
<span data-ttu-id="780c9-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="780c9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780c9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="780c9-125">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780c9-126">CommonParameters</span></span>
<span data-ttu-id="780c9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="780c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780c9-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780c9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="780c9-129">INPUTS</span></span>

### <span data-ttu-id="780c9-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="780c9-130">None</span></span>
<span data-ttu-id="780c9-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="780c9-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="780c9-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="780c9-132">OUTPUTS</span></span>

### <span data-ttu-id="780c9-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="780c9-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="780c9-134">Information om den uppdaterade brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="780c9-134">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="780c9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="780c9-135">NOTES</span></span>

## <span data-ttu-id="780c9-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="780c9-136">RELATED LINKS</span></span>

