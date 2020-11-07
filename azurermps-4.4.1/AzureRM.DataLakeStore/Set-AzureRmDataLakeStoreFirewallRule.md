---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 30a1599468851da5f01e10dc94af6586d3ecaf8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756610"
---
# <span data-ttu-id="ea2f6-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ea2f6-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="ea2f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2f6-103">Ändrar den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ea2f6-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea2f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea2f6-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea2f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ea2f6-106">Cmdleten **set-AzureRmDataLakeStoreFirewallRule** ändrar den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ea2f6-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="ea2f6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea2f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ea2f6-108">Exempel 1: Uppdatera start-och slut adress för en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="ea2f6-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="ea2f6-109">Uppdaterar brand Väggs regeln "MyFirewallRule" i kontot "ContosoADL" för att ha ett område med 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="ea2f6-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="ea2f6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea2f6-110">PARAMETERS</span></span>

### <span data-ttu-id="ea2f6-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="ea2f6-111">-Account</span></span>
<span data-ttu-id="ea2f6-112">Data Lake Store-konto för att uppdatera brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="ea2f6-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f6-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea2f6-113">-EndIpAddress</span></span>
<span data-ttu-id="ea2f6-114">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="ea2f6-114">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f6-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea2f6-115">-Name</span></span>
<span data-ttu-id="ea2f6-116">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="ea2f6-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea2f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea2f6-118">Anger namnet på den resurs grupp som innehåller kontot som ska uppdatera brand Väggs regeln för.</span><span class="sxs-lookup"><span data-stu-id="ea2f6-118">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f6-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea2f6-119">-StartIpAddress</span></span>
<span data-ttu-id="ea2f6-120">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="ea2f6-120">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f6-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea2f6-121">-Confirm</span></span>
<span data-ttu-id="ea2f6-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea2f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea2f6-123">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2f6-124">-DefaultProfile</span></span>
<span data-ttu-id="ea2f6-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea2f6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea2f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2f6-126">CommonParameters</span></span>
<span data-ttu-id="ea2f6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea2f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2f6-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea2f6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2f6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea2f6-129">INPUTS</span></span>

## <span data-ttu-id="ea2f6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea2f6-130">OUTPUTS</span></span>

### <span data-ttu-id="ea2f6-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ea2f6-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="ea2f6-132">Information om den uppdaterade brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="ea2f6-132">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="ea2f6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea2f6-133">NOTES</span></span>

## <span data-ttu-id="ea2f6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea2f6-134">RELATED LINKS</span></span>

