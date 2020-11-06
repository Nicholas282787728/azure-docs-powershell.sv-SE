---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 0cabae7f7b803001a03b64eec027925733d05545
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582168"
---
# <span data-ttu-id="8fd18-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="8fd18-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="8fd18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fd18-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd18-103">Hämtar aktivitet för en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="8fd18-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fd18-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd18-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fd18-105">DESCRIPTION</span></span>
<span data-ttu-id="8fd18-106">Cmdleten **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** hämtar aktivitet för en konfiguration för en SQL-databasserver för återställning av server system.</span><span class="sxs-lookup"><span data-stu-id="8fd18-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="8fd18-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fd18-107">EXAMPLES</span></span>

## <span data-ttu-id="8fd18-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fd18-108">PARAMETERS</span></span>

### <span data-ttu-id="8fd18-109">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8fd18-109">-OperationId</span></span>
<span data-ttu-id="8fd18-110">Anger ID för operationen.</span><span class="sxs-lookup"><span data-stu-id="8fd18-110">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd18-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd18-111">-ResourceGroupName</span></span>
<span data-ttu-id="8fd18-112">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8fd18-112">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd18-113">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8fd18-113">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="8fd18-114">Anger namnet på konfigurationen för återställning av server system.</span><span class="sxs-lookup"><span data-stu-id="8fd18-114">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="8fd18-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8fd18-115">-ServerName</span></span>
<span data-ttu-id="8fd18-116">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="8fd18-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8fd18-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fd18-117">-Confirm</span></span>
<span data-ttu-id="8fd18-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fd18-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd18-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd18-119">-WhatIf</span></span>
<span data-ttu-id="8fd18-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fd18-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd18-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fd18-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd18-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd18-122">-DefaultProfile</span></span>
<span data-ttu-id="8fd18-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd18-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fd18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd18-124">CommonParameters</span></span>
<span data-ttu-id="8fd18-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd18-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd18-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd18-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fd18-127">INPUTS</span></span>

## <span data-ttu-id="8fd18-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fd18-128">OUTPUTS</span></span>

## <span data-ttu-id="8fd18-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fd18-129">NOTES</span></span>

## <span data-ttu-id="8fd18-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fd18-130">RELATED LINKS</span></span>

[<span data-ttu-id="8fd18-131">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="8fd18-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
